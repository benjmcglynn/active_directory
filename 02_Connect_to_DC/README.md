# Connecting a Windows machine to the DC via GUI and PowerShell

-- Connecting via GUI

1. Launch 'Settings'
    - Navigate to 'Accounts'
    - Navigate to 'Access Work or School'
    - Click "Connect" next to 'Add a work or school account'
    - Click 'Join this device to a local Active Directory domain'
    - Enter domain (example.local) and click 'Next'
    - Enter server admin credentials
    - Choose 'standard user' and click 'Next'
    - Machine will restart and will have joined the domain

-- Connecting via PowerShell

2. Launch PowerShell and allow/enter admin credentials if prompted
    '''shell
    Add-Computer -DomainName example.local  -Credential example\administrator -Force -Restart
    '''