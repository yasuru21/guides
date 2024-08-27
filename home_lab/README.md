# Introduction

Setting up a home lab for cybersecurity is an excellent way to practice and develop your skills in a safe, controlled environment. This guide will walk you through the process of setting up virtual machines (VMs) using VirtualBox, a popular virtualization software.

## 1. Install VirtualBox

- Download VirtualBox from the official website (https://www.virtualbox.org/)
- Install VirtualBox on your host machine
- Install VirtualBox Extension Pack for additional features

## 2. Obtain Operating System ISO Files

- Download ISO files for the operating systems you want to use (e.g., Kali Linux, Windows Server, Ubuntu)
- Verify the integrity of downloaded ISO files using checksums

## 3. Create Virtual Machines

- Open VirtualBox and click "New" to create a new VM
- Name your VM and select the appropriate OS type
- Allocate RAM (suggested: 2-4GB for most VMs)
- Create a virtual hard disk (suggested: 20-50GB, dynamically allocated)

## 4. Configure VM Settings

- Select the VM and click "Settings"
- System: Enable I/O APIC, enable hardware clock in UTC time
- Storage: Attach the ISO file to the virtual optical drive
- Network: Set to "NAT Network" for isolated lab environment
- USB: Enable USB 3.0 controller

## 5. Install Operating Systems

- Start the VM and follow the OS installation process
- Install VirtualBox Guest Additions for better performance

## 6. Create Multiple VMs

- Repeat steps 3-5 for different operating systems (e.g., attack machine, target machine)
- Consider creating a pfSense VM for network segmentation

## 7. Network Configuration

- Create a NAT Network in VirtualBox (File > Preferences > Network)
- Assign all VMs to this NAT Network for isolated communication

## 8. Snapshot and Backup

- Take snapshots of clean VM states for easy reset
- Regularly backup your VMs to external storage

## Suggested VirtualBox Settings

- RAM: Allocate at least 25% of your host RAM to VirtualBox
- CPU: Assign 2-4 cores per VM, not exceeding 50% of your total cores
- Storage: Use dynamically allocated VDI files for flexibility
- Network: NAT Network for lab isolation, Bridged Adapter for internet access (NEVER use Bridged for Malware Testing as all your VM's are visibile to your local network)
- Display: Enable 3D Acceleration if supported by guest OS
- Shared Folders: Use with caution in a security lab environment

## Security Considerations

- Keep your host system and VirtualBox up to date
- Use strong passwords for all VMs
- Disable features you're not using (e.g., shared clipboard, drag'n'drop)
- Consider using a dedicated physical machine for your lab if possible

Remember, this home lab is for educational purposes. Always practice ethical hacking and obtain proper authorization before testing on any systems you don't own.
