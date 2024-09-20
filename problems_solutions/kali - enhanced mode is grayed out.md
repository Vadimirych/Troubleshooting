# Enhanced mode is grayed out

# Solution
* Ref: https://www.kali.org/docs/virtualization/install-hyper-v-guest-enhanced-session-mode/
Run command in powershell
**Set-VM "Kali_2024.3" -EnhancedSessionTransportType HVSocket**
