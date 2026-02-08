---
title: "mso 365 ms exchange send from shared email box"
date: 2022-05-03
categories: 
  - "fsse"
---

mso 365 ms exchange send from shared email box

do not add user as member of shared box via GUI use CLI

install CLI

openan elevated PowerShell window (a PowerShell window you open by selecting Run as administrator

Set-ExecutionPolicy RemoteSigned

Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser

REMOVE USER FROM SHARED MAIL BOX (IF YOU HAVE ALREADY ADDED THEM BY MISTAKE)

_Remove-MailboxPermission -Identity -User -AccessRights FullAccess_

  
Remove-MailboxPermission -Identity kathleenr@contoso.onmicrosoft.com -User admin@contoso.onmicrosoft.com -AccessRights FullAccess

ADD USER WITH AUTOMAPPING DISABLED

_Add-MailboxPermission -Identity -User -AccessRights FullAccess -AutoMapping $false_

Add-MailboxPermission -Identity kathleenr@contoso.onmicrosoft.com -User admin@contoso.onmicrosoft.com -AccessRights FullAccess -AutoMapping $false

A SCRIPT TO FIX EVERYONE

$FixAutoMapping = Get-MailboxPermission sharedmailbox |where {$\_.AccessRights -eq "FullAccess" -and $\_.IsInherited -eq $false}  
$FixAutoMapping | Remove-MailboxPermission  
$FixAutoMapping | ForEach {Add-MailboxPermission -Identity $\_.Identity -User $\_.User -AccessRights:FullAccess -AutoMapping $false}
