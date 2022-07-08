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

'''shell
import-Module ADDSDeployment
Install-ADDSForest
'''
    - Set DomainName 'unwindmedia.local'
    - Set SafeModeAdministratorPassword

'''shell
Y to continue (default)
'''
# Server will now need to reboot

3. Set DNS using 'sconfig' back to IP of Domain Controller

# DC is now setup to bare minimum standard

3. Set DNS using PowerShell using the following commands -

    - NetIPAddress
    # finds current IP Address and Interface Index which will be needed
    
    - Set-DNSClientServerAddress -InterfaceIndex (Interface #) -ServerAddresses (DC IP Address)

# DC is now setup to bare minimum standard