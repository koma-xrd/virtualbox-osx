 - install virtualbox 6.1 https://www.virtualbox.org/wiki/Download_Old_Builds_6_1
 - install extension pack 6.1: https://download.virtualbox.org/virtualbox/6.1.40/Oracle_VM_VirtualBox_Extension_Pack-6.1.40.vbox-extpack
 
 - configure USB3.0
 - 2 CPU
 - no floppy disc
 
 
 - installation only with 2 cpu
 - post installation steps:

```
cd "C:\Program Files\Oracle\VirtualBox\"
.\VBoxManage.exe registervm 'C:\Users\fi87roy\VirtualBox VMs\osx13\osx13.vbox'

.\VBoxManage.exe modifyvm "osx13" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff
.\VBoxManage setextradata "osx13" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac19,3"
.\VBoxManage setextradata "osx13" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0"
.\VBoxManage setextradata "osx13" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple"
.\VBoxManage setextradata "osx13" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"
.\VBoxManage setextradata "osx13" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1


// panic reboots
.\VBoxManage setextradata "osx13" "VBoxInternal/TM/TSCMode" "RealTSCOffset"
```
