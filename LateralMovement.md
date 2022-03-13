# Lateral Movement

## PowerShell Remoting

 - One-to-One
 - PSSession 
   - Interactive
   - Runs in a new process (wsmprovhost)
   - Is stateful
 - Useful cmdlets
   - New-PSSession (stateful-does not create new session)
   - Enter-PSSession (create new session)

 ## Commands

 ```powershell
 $creds = Get-Credential
 $sess = New-PSSession -ComputerName test.com -Credential $creds
 Enter-PSSession $sess
 ```

## PowerShell Remoting

 - One-to-Many
 - Also known as Fan-out remoting.
 - Non-interactive.
 - Executes commands parallely.
 - Userful cmdlets
   - Invoke-command