# Setting up the Domain Controller 

1. Use 'sconfig' to:
    - Change the hostname
    - Change the IP Address (if needed) and set to Static
    - Set the default gateway
    - Change the DNS server to IP Address of machine 
 
2. Install the Active Directory Service

'''shell
Install-WindowsFeature AD-DomainServices -IncludeManagementTools
'''