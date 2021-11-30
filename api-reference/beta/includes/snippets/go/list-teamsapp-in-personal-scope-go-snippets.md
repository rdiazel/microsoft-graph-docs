---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &msgraphsdk.TeamsAppsRequestBuilderGetQueryParameters{
	Expand: "appDefinitions($select=id,displayName,allowedInstallationScopes)",
	Filter: "appDefinitions/any(a:a/allowedInstallationScopes%20has%20'personal')",
}
options := &msgraphsdk.TeamsAppsRequestBuilderGetOptions{
	Q: requestParameters,
}
result, err := graphClient.AppCatalogs().TeamsApps().Get(options)


```