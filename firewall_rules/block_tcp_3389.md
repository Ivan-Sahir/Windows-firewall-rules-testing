# Block TCP Port 3389 in Windows Defender Firewall

This rule blocks all incoming traffic to TCP port 3389 on the Windows host, preventing Remote Desktop (RDP) access from the VM or any other devices on the network.

# Purpose

To prevent unauthorized Remote Desktop access, which is commonly exploited for lateral movement, brute-force attacks, or unauthorized remote control.

<img width="441" height="589" alt="{46D20CBD-2A24-48FF-8A21-8CC765B742B3}" src="https://github.com/user-attachments/assets/5c0a50f5-ac47-4d46-9dfc-fb41da90ddec" />

# Expected Behavior

- When scanning the Windows host from the VM, port 3389 will appear as **filtered** or **closed**.
- RDP services will not be reachable from the VM.
- Nmap or other scanners will show no response from this port.

<img width="757" height="106" alt="{0D1DC85B-35A3-40DD-AAD2-8869CEBE1859}" src="https://github.com/user-attachments/assets/e2a282e8-0773-4161-932e-3240196afb6b" />


# Verification

Check from the VM with:
```bash
nmap -p 3389 <windows_host_ip>
