---
title: "Exchange Online PowerShell V2 module"
date: 2022-05-03
categories: 
  - "fsse"
---

PS C:\\Windows\\system32> Install-Module -Name ExchangeOnlineManagement

NuGet provider is required to continue  
PowerShellGet requires NuGet provider version '2.8.5.201' or newer to interact with NuGet-based repositories. The NuGet provider must be available in 'C:\\Program  
Files\\PackageManagement\\ProviderAssemblies' or 'C:\\Users\\CliveDarracott\\AppData\\Local\\PackageManagement\\ProviderAssemblies'. You can also install the NuGet provider by running

'Install-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force'. Do you want PowerShellGet to install and import the NuGet provider now?  
\[Y\] Yes \[N\] No \[S\] Suspend \[?\] Help (default is "Y"):

ExchangeOnlineManagement 2.0.5  
This is a General Availability (GA) release of Exchange Online PowerShell V2 module.

Install-Module -Name ExchangeOnlineManagement -RequiredVersion 2.0.5

https://docs.microsoft.com/en-us/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps

https://docs.microsoft.com/en-us/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps#install-and-maintain-the-exo-v2-module

DISABLE AUTOMAP

https://docs.microsoft.com/en-us/previous-versions/office/exchange-server-2010/hh529943(v=exchg.141)

GET MAILBOX PERM

https://docs.microsoft.com/en-us/powershell/module/exchange/get-mailboxpermission?view=exchange-ps

Get-MailboxPermission -Identity john@contoso.com | Format-List

REMOVE MAILBOX PERM

https://docs.microsoft.com/en-us/outlook/troubleshoot/profiles-and-accounts/remove-automapping-for-shared-mailbox#:~:text=%20To%20do%20this%2C%20follow%20these%20steps%3A%20,To%20do%20this%2C%20at%20the%20command…%20See%20More.

Remove-MailboxPermission -Identity -User -AccessRights FullAccess

Remove-MailboxPermission -Identity kathleenr@contoso.onmicrosoft.com -User admin@contoso.onmicrosoft.com -AccessRights FullAccess

ADD MAILBOX PERM

Add-MailboxPermission -Identity -User -AccessRights FullAccess -AutoMapping $false

Add-MailboxPermission -Identity kathleenr@contoso.onmicrosoft.com -User admin@contoso.onmicrosoft.com -AccessRights FullAccess -AutoMapping $false
