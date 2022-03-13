# Common Hurdles in AD 

## AppLocker
 
Identify the local AppLocker policy. Look for exempted binaries such as Microsoft signed windows binaries and scripts or paths to bypass.

```powershell
Get-AppLockerPolicy -Effective | select -ExpandProperty RuleCollections
```

Get a remote AppLocker policy, based on the Distinguished Name of the respective Group Policy. Use the Get-NetGPO -DomainController or -ComputerName to get the adspath e.g               : "LDAP://CN={211A25B2-03AD-4E5E-9C6A-AFEFE66EFB2D},CN=Policies,CN=System,DC=dollarcorp,DC=moneycorp,DC=local"
and used it as a parameter on Get-AppLockerPolicy.

```powershell
PS C:\Users\student26> Get-NetGPO -ComputerName dcorp-adminsrv.dollarcorp.moneycorp.local
```

```powershell
Get-AppLockerPolicy -Domain -LDAP "LDAP://targetdomain.com/CN={16641EA1-8DD3-4B33-A17F-9F259805B8FF},CN=Policies,CN=System,DC=targetdomain,DC=com"  | select -expandproperty RuleCollections
```

## PowerShell Constrained Language Mode

Constrained Language Mode or CLM is a policy that can be observed when  Applocker was present to an AD environment. It can be checked using the following and will output FullLanguage if unrestricted and ConstrainedLanguage if restricted.

```powershell
$ExecutionContext.SessionState.LanguageMode
```

Some high-level bypass techniques:

- Use LOLBAS if only (Microsoft-)signed binaries are allowed.

- If binaries from C:\Windows are allowed (default behavior), try dropping your binaries to C:\Windows\Temp or C:\Windows\Tasks. If there are no writable subdirectories but writable files exist in this directory tree, write your file to an alternate data stream (e.g. a JScript script) and execute it from there.

- Wrap your binaries in a DLL file and execute them with rundll32 to bypass executable rules if DLL execution is not enforced (default behavior).

- If binaries like Python are allowed, use those. If that doesn’t work, try other techniques such as wrapping JScript in a HTA file or running XSL files with wmic.

- Otherwise elevate your privileges. AppLocker rules are most often not enforced for (local) administrative users.