# Disable Anti-malware

## Use Registry Key

### Using reg Command
* Run following command as an Administrator

```
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1
```

### Using regedit.exe

1. From the following registry key:

> HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender

2. New,  DWORD (32-bit) Value and name it DisableAntiSpyware

> Set the value from to 1


### Reg Key Run

* Download [DisableWindowsDefender.reg](WindowsDefender/DisableWindowsDefender.reg) and run on the target virtual machine.

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender]
"DisableAntiSpyware"=dword:00000001
```

## Use Group Policy Editor: Computer Configuration

* Run "gpedit.msc"

* Under Computer Configuration / Administrative Templates / Windows Components / Windows Defender Antivirus
  - Look for turn off windows defender antivirus 
    - Select Enabled 
