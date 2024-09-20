# Kali - Enhanced mode is grayed out in Hyper-V

# Problem - Enhanced mode is disabled

# Solution
* Ref: https://www.kali.org/docs/virtualization/install-hyper-v-guest-enhanced-session-mode/

Run command in powershell with admin priveleges
```
Set-VM "Kali_2024.3" -EnhancedSessionTransportType HVSocket
```
