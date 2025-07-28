# Windows-firewall-rules-testing

# Windows Defender Firewall Rules Testing

I made this project to create and test custom Windows Defender Firewall rules using a VirtualBox virtual machine as a test environment.

# Objective

- Configure various Windows Firewall rules on a Windows host.
- Use a Windows 10 VM to simulate external traffic.
- Validate rules with tools like ping, Nmap

# Rules Covered

- Block ICMP Echo Requests
- Block TCP port 3389
- Block all traffic from VM's IP

# VM Setup

A basic Ubuntu VM is used for testing. Setup instructions are included in [`vm_setup/virtualbox_vm_setup.md`](vm_setup/virtualbox_vm_setup.md).

# Tools Used

- Windows Defender Firewall (`wf.msc`)
- Nmap (on VM)
- Ping

