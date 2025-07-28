# Block ICMP Echo Requests in Windows Defender Firewall

This rule blocks all incoming ICMP Echo Requests (ping requests) to the Windows host, preventing it from responding to ping attempts from the VM or other devices on the network.

# Purpose

To increase security by disabling ping replies, which can reduce host visibility on the network.


# Expected Behavior

- When pinging the Windows host from the VM, no reply will be received.
- The ping command will show 100% packet loss or “Request timed out.”

<img width="698" height="261" alt="{0A2DE8EA-EF43-40A3-AFA8-912F2C4D8718}" src="https://github.com/user-attachments/assets/0116a244-5a7a-4563-9231-5bcf08e53c26" />


# Verification

Check from the VM with:
```bash
ping <windows_host_ip>
