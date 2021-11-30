---
title: "Use Microsoft Graph to configure required Azure AD Graph permissions for an app registration"
description: "Use Microsoft Graph to configure required Azure AD Graph permissions for an app registration."
author: "FaithOmbongi"
ms.localizationpriority: medium
ms.prod: "applications"
---

# Use Microsoft Graph to configure required Azure AD Graph permissions for an app registration

Azure Active Directory (Azure AD) Graph is deprecated and will be retired on June 30, 2022. As part of this deprecation path, adding Azure AD Graph permissions to the required permissions for an app registration through the Azure portal is now disabled. We recommend that you follow the [App migration planning checklist](migrate-azure-ad-graph-planning-checklist.md) to help you transition your apps to the [Microsoft Graph](/graph/overview) API.

However, you might still need to add more Azure AD Graph permissions to your app. This article provides you with guidance for using Microsoft Graph to configure required permissions for Azure AD Graph to your app registration.

> [!CAUTION]
> Any app using Azure AD Graph will still stop functioning after June 30, 2022. For more information, see [Migrate Azure AD Graph apps to Microsoft Graph](migrate-azure-ad-graph-overview.md).

## Option 1: Use the Microsoft Graph API

The Microsoft Graph [application](/graph/api/resources/application) API includes a **requiredResourceAccess** property that is a collection of  [requiredResourceAccess](/graph/api/resources/requiredresourceaccess) objects. Use this property to configure required Azure AD Graph permissions as described in the following steps.

### Prerequisites

To complete the following steps, you need the following resources and privileges:

+ Run the HTTP requests in a tool of your choice, for example in your app, through [Graph Explorer](https://aka.ms/ge), or Postman.
+ Run the APIs as a user in a Global Administrator or Application Administrator role, or as owner of the target app registration. For more information about the actions supported by these roles, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference).
+ The app used to make these changes must be granted the `Application.ReadWrite.All` permission.

### Step 1: Identify the permission IDs for the Azure AD Graph permissions your app requires

Identify the Azure AD Graph permissions your app requires, their permission IDs, and whether they are app roles (application permissions) or delegated permissions. You can retrieve the permission IDs from an existing app registration that has the permission configured by reading its **requiredResourceAccess** property either in the app's **Manifest** on the Azure portal, or through the Microsoft Graph API. 

Azure AD Graph's globally unique **appId** is `00000002-0000-0000-c000-000000000000` and it's identified by the **resourceAppId** property of the **requiredResourceAccess** property.

### Request

The following request retrieves Azure AD Graph permission IDs and types from an existing application identified by **id** `f7748341-825c-46e9-a111-5e3b56ae015b`.

<!-- {
  "blockType": "request",
  "name": "migrate-azureadgraph-get-serviceprincipal-azureadgraph"
}-->

```msgraph-interactive
https://graph.microsoft.com/v1.0/applications/f7748341-825c-46e9-a111-5e3b56ae015b?$select=requiredResourceAccess
```

### Response

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.servicePrincipal"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#applications(requiredResourceAccess)/$entity",
    "requiredResourceAccess": [
        {
            "resourceAppId": "00000002-0000-0000-c000-000000000000",
            "resourceAccess": [
                {
                    "id": "311a71cc-e848-46a1-bdf8-97ff7156d8e6",
                    "type": "Scope"
                },
                {
                    "id": "3afa6a7d-9b1a-42eb-948e-1650a849e176",
                    "type": "Role"
                }
            ]
        }
    ]
}
```

From this output, `311a71cc-e848-46a1-bdf8-97ff7156d8e6` is the permission ID of the *User.Read* delegated permission while `3afa6a7d-9b1a-42eb-948e-1650a849e176` is the permission ID of the *Application.Read.All* app role.

### Step 2: Add required Azure AD Graph permissions to your app

The following example calls the [Update application](/graph/api/application-update) API to add the required Azure AD Graph permissions to an app registration identified by object ID `581088ba-83c5-4975-b8af-11d2d7a76e98`. From Step 1, these permissions were *User.Read* and *Application.Read.All* delegated permission and app role respectively.

> [!IMPORTANT]
> To update the **requiredResourceAccess** property, you must pass in both existing and new permissions. Passing in only new permissions overwrites and removes the existing permissions.

#### Request

<!-- {
  "blockType": "request",
  "name": "migrate-azureadgraph-update-application"
}-->
```msgraph-interactive
PATCH https://graph.microsoft.com/v1.0/applications/581088ba-83c5-4975-b8af-11d2d7a76e98
Content-Type: application/json

{
    "requiredResourceAccess": [
        {
            "resourceAppId": "00000002-0000-0000-c000-000000000000",
            "resourceAccess": [
                {
                    "id": "311a71cc-e848-46a1-bdf8-97ff7156d8e6",
                    "type": "Scope"
                },
                {
                    "id": "3afa6a7d-9b1a-42eb-948e-1650a849e176",
                    "type": "Role"
                }
            ]
        }
    ]
}
```

#### Response

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

### Step 3: Verify that the required Azure AD Graph permissions were added to your app

Verify that your app registration has the required API permissions you added in Step 2 by using the Microsoft Graph API or by checking the **App registrations** page in the Azure portal.

#### Use the Microsoft Graph GET /application/{id} API

The following request retrieves the **id** and **requiredResourceAccess** properties of the app identified by object **id** `581088ba-83c5-4975-b8af-11d2d7a76e98`.

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/applications/581088ba-83c5-4975-b8af-11d2d7a76e98?$select=id,requiredResourceAccess
```

>**Note:** Though you've configured the permissions the app requires, these permissions haven't been granted. Many permissions require admin consent before they can be used to access organizational data.

## Option 2: Use Microsoft Graph PowerShell

The [Update-MgApplication](/powershell/module/microsoft.graph.applications/update-mgapplication?view=graph-powershell-1.0&preserve-view=true) cmdlet in Microsoft Graph PowerShell includes a **RequiredResourceAccess** parameter that is a collection of **IMicrosoftGraphRequiredResourceAccess** objects. Use this parameter to configure the required Azure AD Graph permissions as described in the following steps.

### Prerequisites

To complete the following steps, the following privileges are required:

+ An authenticated PowerShell session (for example, using `Connect-MgGraph`).
+ Microsoft Graph PowerShell must be granted the `Application.ReadWrite.All` permission.
+ The signed-in user must be granted the Global Administrator or Application Administrator Azure AD directory roles, or be owner of the target app registration. For more information about the actions supported by these roles, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference).

### Step 1: Identify the permission IDs for the Azure AD Graph permissions your app requires

Identify the Azure AD Graph permissions your app requires, their permission IDs, and whether they are app roles (application permissions) or delegated permissions. You can retrieve the permission IDs from an existing app registration that has the permission configured by reading its **RequiredResourceAccess** property either in the app's **Manifest** on the Azure portal, or through a PowerShell script.

### Request

Create a new PowerShell script named **fetchPermissions.ps1** and add the following code. This code retrieves Azure AD Graph permission IDs and types from an existing app registration identified by object ID `f7748341-825c-46e9-a111-5e3b56ae015b`. Replace `f7748341-825c-46e9-a111-5e3b56ae015b` with your source app's object ID.

```powershell
# Sign in with the required Application.ReadWrite.All scope
Connect-Graph -Scopes "Application.ReadWrite.All" 

## Replace f7748341-825c-46e9-a111-5e3b56ae015b with the object ID of the existing app registration; then read and output the permission IDs and their types
$sourceAppId= 'f7748341-825c-46e9-a111-5e3b56ae015b' 
$sourceApp = Get-MgApplication -ApplicationId $sourceAppId 
$sourceApp.RequiredResourceAccess.ResourceAccess
```

Run the script using the following command
```powershell
.\fetchPermissions.ps1
```

### Response

The following is an example of the output.

```powershell
Id                                   Type
--                                   ----
311a71cc-e848-46a1-bdf8-97ff7156d8e6 Scope
3afa6a7d-9b1a-42eb-948e-1650a849e176 Role
```

From this output, `311a71cc-e848-46a1-bdf8-97ff7156d8e6` is the permission ID of the *User.Read* delegated permission while `3afa6a7d-9b1a-42eb-948e-1650a849e176` is the permission ID of the *Application.Read.All* app role.

### Step 2: Add Azure AD Graph permissions to your app

Create a new PowerShell script named **updatePermissions.ps1** and add the following code. This code adds the required Azure AD Graph permissions to an app registration identified by object ID `581088ba-83c5-4975-b8af-11d2d7a76e98`. From Step 1, these permissions were *User.Read* and *Application.Read.All* delegated permission and app role respectively.

> [!IMPORTANT]
> To update the **RequiredResourceAccess** property, you must pass in both existing and new permissions. Passing in only new permissions overwrites and removes the existing permissions.

#### Request

```powershell
# Sign in with the required Application.ReadWrite.All scope
Connect-Graph -Scopes "Application.ReadWrite.All" 

## Replace 581088ba-83c5-4975-b8af-11d2d7a76e98 with the object ID of the app you wish to add new permissions to
$applicationId = '581088ba-83c5-4975-b8af-11d2d7a76e98' 

$app = Get-MgApplication -ApplicationId $applicationId

## Azure AD Graph's globally unique appId is 00000002-0000-0000-c000-000000000000 identified by the ResourceAppId
$aadAccess = $app.RequiredResourceAccess | Where-Object { $_.ResourceAppId -eq '00000002-0000-0000-c000-000000000000' } 

if($null -eq $aadAccess){ 
    $app.RequiredResourceAccess += @{  
        ResourceAppId = "00000002-0000-0000-c000-000000000000"; 
        ResourceAccess = @( 

                ## Replace the following with values of ID and type for all permissions - both new and existing permissions - you want to configure for the app
                @{ 
                    # User.Read delegated permission Sign in and read user profile 
                    id = "311a71cc-e848-46a1-bdf8-97ff7156d8e6";  
                    type = "Scope"; 
                }, 
                @{ 
                    # Application.Read.All app role (application permission) to view application data
                    id = "3afa6a7d-9b1a-42eb-948e-1650a849e176"; 
                    type = "Role"; 
                }
            ) 
     } 
} 

Update-MgApplication -ApplicationId $applicationId -RequiredResourceAccess $app.RequiredResourceAccess 
```

Run the script using the following command.
```powershell
.\updatePermissions.ps1
```

### Response

The following is an example of the output.

```powershell
Welcome To Microsoft Graph!
```

>**Note:** Though you've configured the permissions the app requires, these permissions haven't been granted. Many permissions require admin consent before they can be used to access organizational data.

## See also

+ [application API](/graph/api/resources/application)
+ [Update-MgApplication](/powershell/module/microsoft.graph.applications/update-mgapplication?view=graph-powershell-1.0&preserve-view=true)
