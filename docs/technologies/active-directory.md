The main domain controller is the DC1 machine running Windows Server 2025, while the backup domain controller is DC2. The forest name is HOMELAB.LOCAL and contains only one root domain. Inside it we have several OUs organized in the following manner 

```
HOMELAB.LOCAL
    - Departments
        - IT
            - IT-Users
            - IT-Computers
        - Sales
            - Sales-Users
            - Sales-Computers
        - Management
            - Sales-Users
            - Sales-Computers
    - Service Accounts
    - Servers 
    - Groups
```

Other machines that have been joined to the domain are a couple of windows clients and a windows server.

## Tasks performed (GUI and/or Powershell)
- Install ADDS role
- Create forest/domain
- Add and remove users and groups
- Add and remove GPOs 
### GPOs
- "Enable Remote Desktop Connection" : allows users to connect using Remote Desktop Services, add firewall rule for inbound RDP traffic, add memebers of security group to local Remote Desktop Users group.

