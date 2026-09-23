---
type: cat
id: cat_ab1c1882
title: Microsoft is updating its author-signing certificate starting September 23, 2026
resource: https://devblogs.microsoft.com/dotnet/microsoft-author-signing-certificate-update-2026/
t_confidence: 0.6499999999999999
t_relevance: 0.7
t_signal: 0.6
t_reading_minutes: 2
horizon: read-today
lane: tech
timestamp: 2026-09-23T22:00:44.7960569+00:00
published_at: 2026-09-23T20:00:00.0000000+00:00
excerpt: 'Action required: If you validate that packages are author-signed by Microsoft using a NuGet client policy or the dotnet nuget verify command, follow the steps in this post as soon as possible to avoid potential disruptions during the transition. If you are unsure whether you are impacted, follow the steps below to check. Microsoft uses an X.509 certificate to author-sign its NuGet packages. As soon as September 23, 2026, a new certificate will become the default Microsoft author-signing certificate for NuGet packages. Existing packages signed with an older certificate will retain their signatures, but the current certificate will no longer be used to sign new packages after the transition. Current certificate SHA-256 fingerprint: 566A31882BE208BE4422F7CFD66ED09F5D4524A5994F50CCC8B05EC0528C1353 New certificate SHA-256 fingerprint: 9A1B131BEE0605433056A4EA3815478A8E177961A968C6C0027C1093D1FEB630 Who will be impacted? Customers who use a NuGet client policy to enforce an allow list of trusted signers that includes Microsoft. To determine whether you have a NuGet client policy configured, check for the following elements in your nuget.config . Keep in mind that nuget.config files can exist in multiple locations with different scopes . Customers who use dotnet nuget verify to verify that signed packages are author-signed by Microsoft. This may look like the following: dotnet nuget verify --certificate-fingerprint 3F9001EA83C560D712C24CF213C3D312CB3BFF51EE89435D3430BD06B5D0EECE --certificate-fingerprint AA12DA22A49BCE7D5C1AE64CC1F3D892F150DA76140F210ABD2CBFFCA2C18A27 --certificate-fingerprint 566A31882BE208BE4422F7CFD66ED09F5D4524A5994F50CCC8B05EC0528C1353 If neither scenario applies to you, you should be unaffected by this certificate update. Microsoft NuGet packages signed with the new certificate should install in the same way as packages signed with older certificates. Allow the new Microsoft certificate Client policy If you use a NuGet client policy to enforce an allow list of trusted signers, add the new Microsoft certificate to the allow list as soon as possible. Keep the older Microsoft certificates in the policy so that you can continue to install packages signed with those certificates. If you try to install a package signed with the new certificate without updating your trusted signers, the package installation will fail with an NU3034 error. You can add the new Microsoft author-signing certificate by running the following command: dotnet nuget trust author Microsoft 9A1B131BEE0605433056A4EA3815478A8E177961A968C6C0027C1093D1FEB630 --algorithm SHA256 The dotnet nuget trust command is available in the .NET 6 SDK and later. It updates the applicable nuget.config file. Use --configfile to update a specific configuration file. Alternatively, add the new certificate to the existing Microsoft entry in nuget.config . The resulting entry should include both the older certificates and the new certificate: Package verification If you use dotnet nuget verify to confirm that a signed package is author-signed by Microsoft, add the new fingerprint while retaining the older fingerprints: dotnet nuget verify --certificate-fingerprint 3F9001EA83C560D712C24CF213C3D312CB3BFF51EE89435D3430BD06B5D0EECE --certificate-fingerprint AA12DA22A49BCE7D5C1AE64CC1F3D892F150DA76140F210ABD2CBFFCA2C18A27 --certificate-fingerprint 566A31882BE208BE4422F7CFD66ED09F5D4524A5994F50CCC8B05EC0528C1353 --certificate-fingerprint 9A1B131BEE0605433056A4EA3815478A8E177961A968C6C0027C1093D1FEB630 Each --certificate-fingerprint option adds an accepted SHA-256 signer certificate fingerprint. Keeping all four values allows the command to verify newly signed packages and existing packages signed with an older Microsoft certificate. Feedback If you have questions about how you may be impacted or run into issues while following these steps, please contact us . For more general NuGet feedback and suggestions: Review our guidance for submitting bugs and suggestions . Start a discussion or open an issue in the NuGet/Home repository . The post Microsoft is updating its author-signing certificate starting September 23, 2026 appeared first on .NET Blog .'
t_source: source_dotnet
author: The NuGet Team
t_suggested_tags:
- topic/csharp
- topic/dotnet
- topic/typescript
...
---
## Summary

Summary: Microsoft is updating its author-signing certificate starting September 23, 2026
