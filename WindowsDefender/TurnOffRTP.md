# Turn off Anti-malware real time protection
Please turn off any Anti-malware products' real-time detection before performing any tests

   * For example, for Windows Defender, run following command from a PowerShell prompt with Administrator privilege

```
Set-MpPreference -DisableRealtimeMonitoring $true
```

