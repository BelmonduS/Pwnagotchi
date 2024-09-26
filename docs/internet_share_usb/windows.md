https://raw.githubusercontent.com/evilsocket/pwnagotchi/master/scripts/win_connection_share.ps1


https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.4

PS C:\WINDOWS\system32> C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1
File C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 cannot be loaded. The file C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 is not digitally signed. You cannot run this script on the current system. For more information about
running scripts and setting execution policy, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
+ CategoryInfo          : SecurityError: (:) [], ParentContainsErrorRecordException
+ FullyQualifiedErrorId : UnauthorizedAccess

PS C:\WINDOWS\system32> C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1
File C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 cannot be loaded. The file C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 is not digitally signed. You cannot run this script on the current system. For more information about
running scripts and setting execution policy, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
+ CategoryInfo          : SecurityError: (:) [], ParentContainsErrorRecordException
+ FullyQualifiedErrorId : UnauthorizedAccess

PS C:\WINDOWS\system32> Get-ExecutionPolicy -Scope CurrentUser
Undefined

PS C:\WINDOWS\system32> Get-ExecutionPolicy
RemoteSigned

PS C:\WINDOWS\system32> Set-ExecutionPolicy -ExecutionPolicy Unrestricted

PS C:\WINDOWS\system32> C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1
C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 : By default Internet Connection Sharing uses a 192.168.137.x subnet. Run this script with the -SetPwnagotchiSubnet to setup the network.
+ CategoryInfo          : NotSpecified: (:) [Write-Error], WriteErrorException
+ FullyQualifiedErrorId : Microsoft.PowerShell.Commands.WriteErrorException,win_connection_share.ps1


PS C:\WINDOWS\system32> C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 -EnableInternetConnectionSharing
C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 : By default Internet Connection Sharing uses a 192.168.137.x subnet. Run this script with the -SetPwnagotchiSubnet to setup the network.
At line:1 char:1
+ C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 -EnableI ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Write-Error], WriteErrorException
    + FullyQualifiedErrorId : Microsoft.PowerShell.Commands.WriteErrorException,win_connection_share.ps1


PS C:\WINDOWS\system32>  C:\Users\belmondus\OneDrive\Desktop\win_connection_share.ps1 -EnableInternetConnectionSharing -SetPwnagotchiSubnet
WARNING: The Internet Connection Sharing subnet has been updated. A reboot of windows is required !
Please select your main a ethernet adaptor with internet access that will be used for internet sharing.
[1] Ethernet 5, USB Ethernet/RNDIS Gadget #3
[2] Ethernet, Killer E3100G 2.5 Gigabit Ethernet Controller
[3] VMware Network Adapter VMnet1, VMware Virtual Ethernet Adapter for VMnet1
[4] VMware Network Adapter VMnet8, VMware Virtual Ethernet Adapter for VMnet8
Number: 2
Please select your 'USB Ethernet/RNDIS Gadget' adaptor
[1] Ethernet 5, USB Ethernet/RNDIS Gadget #3
[2] Ethernet, Killer E3100G 2.5 Gigabit Ethernet Controller
[3] VMware Network Adapter VMnet1, VMware Virtual Ethernet Adapter for VMnet1
[4] VMware Network Adapter VMnet8, VMware Virtual Ethernet Adapter for VMnet8
Number: 1
[x] Enabled Internet Connection Sharing.

PS C:\WINDOWS\system32> 