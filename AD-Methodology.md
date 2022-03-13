# AD Methodology


1. Assume we have the foothold and we have a domain user with low privileges on the machine. First thing to do is to escalate our privileges to administrator or system.
   
   	What to look for?

   - What is the AMSI/ EDR solution/ AV in the host?

   - What are the ways we can escalate to administrator or system?

   - What are the policies in placed by looking at the applocker.

     - ```Get-AppLockerPolicy -Effective | select -ExpandProperty RuleCollections```

     - 

2. Assume we have the system or admin privileges on the foothold machine, we can enumerate other machines that our current user has a local admin priviliges using PowerView.ps1.

 What commands I can use?

  - ```Find-LocalAdminAccess``` 


3. We can look for a specfic user or hunt for a domain admins user where it has a session. Admin privileges are not needed

  - ```Invoke-UserHunter -CheckAccess```

  - ```Invoke-UserHunter -Stealth``` 

