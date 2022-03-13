# Privilege Escalation

## There are various ways of locally escalating privileges on Windows box:

 - Missing patches
 - Automated deployment and AutoLogon passwords in clear text
 - AlwaysInstallElevated (Any user can run MSI as SYSTEM)
 - Misconfigured Services
 - DLL Hijacking and More

## We can use below tools for complete coverage

 - PowerUp:https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc
 - BeRoot:https://github.com/AlessandroZ/BeRoot
 - Privesc:https://github.com/enjoiz/Privesc

## Services issues using PowerUp

```powershell
Get-ServiceUnquoted -Verbose
```
## Get services where the current user can write to its binary path or change arguments to the binary

```powershell
Get-ModifiableServiceFile -Verbose
```
## Get the services whose configuration current user can modify.

```powershell
Get-ModifiableService -Verbose
```