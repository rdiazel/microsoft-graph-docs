# Generate a certificate for your application

## Use Powershell

```powershell
$cert = New-SelfSignedCertificate -Subject "CN=certificateName" -CertStoreLocation "Cert:\CurrentUser\My" -KeyExportPolicy Exportable -KeySpec Signature -KeyLength 2048 -KeyAlgorithm RSA -HashAlgorithm SHA256 
```

## [Use C#](#tab/csharp)

```csharp
using System;
using System.Security.Cryptography;
using System.Security.Cryptography.X509Certificates;
using System.Text;
    /* CONSOLE APP - PROOF OF CONCEPT CODE ONLY!!
     * This code uses a self-signed certificate and should not be used 
     * in production. This code is for reference and learning ONLY.
     */
namespace Self_signed_cert
{
    class Program
    {
        static void Main(string[] args)
        {
            // Generate a guid to use as a password and then create the cert.
          string password = Guid.NewGuid().ToString();
          var selfsignedCert = buildSelfSignedServerCertificate(password);
          // Print values so we can copy paste into the JSON fields.
            // Print out the private key in base64 format.
          Console.WriteLine("Private Key: {0}{1}", Convert.ToBase64String(selfsignedCert.Export(X509ContentType.Pfx, password)), Environment.NewLine);
          // Print out the start date in ISO 8601 format.
          DateTime startDate = DateTime.Parse(selfsignedCert.GetEffectiveDateString()).ToUniversalTime();
          Console.WriteLine("startDateTime: " + startDate.ToString("o"));
          // Print out the end date in ISO 8601 format.
          DateTime endDate = DateTime.Parse(selfsignedCert.GetExpirationDateString()).ToUniversalTime();
          Console.WriteLine("endDateTime: " + endDate.ToString("o"));
          // Print the GUID used for keyId
          string signAndPasswordGuid = Guid.NewGuid().ToString();
          string verifyGuid = Guid.NewGuid().ToString();
          Console.WriteLine("keyId GUID for Sign and passwordCredentials: " + signAndPasswordGuid);
          Console.WriteLine("keyId GUID for Verify: " + verifyGuid);
          // Print out the password.
          Console.WriteLine("Password: {0}", password);
          // Print out a displayName to use as an example.
          Console.WriteLine("displayName: CN=Example");
          Console.WriteLine();
          // Print out the public key.
          Console.WriteLine("Public Key: {0}{1}", Convert.ToBase64String(selfsignedCert.Export(X509ContentType.Cert)), Environment.NewLine);
          Console.WriteLine();
          // Generate the customKeyIdentifier using hash of thumbprint.
          Console.WriteLine("Cert thumprint: {0}{1}", selfsignedCert.Thumbprint, Environment.NewLine);
          Console.WriteLine("customKeyIdentifier:");
          string keyIdentifier = GetSha256FromThumbprint(selfsignedCert.Thumbprint);
          Console.WriteLine(keyIdentifier);
        }
        // Generate a self-signed certificate.
        private static X509Certificate2 buildSelfSignedServerCertificate(string password)
        {
          const string CertificateName = @"Microsoft Azure Federated SSO Certificate TEST";
          DateTime certificateStartDate = DateTime.UtcNow;
          DateTime certificateEndDate = certificateStartDate.AddYears(2).ToUniversalTime();
          X500DistinguishedName distinguishedName = new X500DistinguishedName($"CN={CertificateName}");
          using (RSA rsa = RSA.Create(2048))
          {
            var request = new CertificateRequest(distinguishedName, rsa, HashAlgorithmName.SHA256, RSASignaturePadding.Pkcs1);
            request.CertificateExtensions.Add (
              new X509KeyUsageExtension(X509KeyUsageFlags.DataEncipherment | X509KeyUsageFlags.KeyEncipherment | X509KeyUsageFlags.DigitalSignature, false)
            );
            var certificate = request.CreateSelfSigned(new DateTimeOffset(certificateStartDate), new DateTimeOffset(certificateEndDate));
                certificate.FriendlyName = CertificateName;
            return new X509Certificate2(certificate.Export(X509ContentType.Pfx, password), password, X509KeyStorageFlags.Exportable);
            }
        }
        // Generate hash from thumbprint.
        public static string GetSha256FromThumbprint(string thumbprint)
        {
          var message = Encoding.ASCII.GetBytes(thumbprint);
          SHA256Managed hashString = new SHA256Managed();
          return Convert.ToBase64String(hashString.ComputeHash(message));
        }
    }
}
```

## [Use Java](#tab/java)




---