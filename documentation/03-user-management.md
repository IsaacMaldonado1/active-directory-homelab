# Domain Controller Setup

## Overview
I set up a Windows Server 2025 VM to practice Active Directory administration for a small company network.

## Setup
- Server name: DT-DC01
- OS: Windows Server 2025 Evaluation
- Virtualization: QEMU/KVM on Ubuntu
- Domain: dentech.local
- Network: Default NAT

## Configuration
I installed Active Directory Domain Services and configured the server as the first domain controller in a new forest.

DNS is being used to help domain-joined computers find the domain controller and other domain services.

## Testing
- [ ] Confirm the server name
- [ ] Verify the domain was created
- [ ] Check that Active Directory Users and Computers opens
- [ ] Verify the DNS service is running
- [ ] Test a domain login from the Windows 11 VM

## Notes
I'll add any issues I run into and how I fixed them as I continue building the lab.
