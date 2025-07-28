# Block All Traffic from VM in Windows Defender Firewall

This rule blocks all inbound traffic to the Windows host from the VM's specific IP address, preventing any communication attempts such as pings, port scans, or service connections.

# Purpose

To simulate a scenario where a host needs to block a specific untrusted device (like a compromised system) from the network entirely.

# Expected Behavior

- All traffic from the VM to the Windows host will be blocked.
- Any service requests will fail or show 100% packet loss / filtered.
- The VM will not be able to detect the host via any common protocol.

<img width="828" height="99" alt="{038C9F59-2EC7-4964-BA2A-8DD1C38DA0BF}" src="https://github.com/user-attachments/assets/39d3aebe-72a6-4e38-8651-c03239dee70c" />

# Verification

From the VM:
```bash
nmap -p 1-1000 <windows_host_ip>
