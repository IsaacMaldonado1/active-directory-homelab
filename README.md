# Active Directory Homelab

A Windows Server 2025 lab built with QEMU/KVM to practice core Windows administration tasks in a small, fictional business environment.

## Lab Overview

- **Server OS:** Windows Server 2025 Evaluation
- **Virtualization host:** Ubuntu with QEMU/KVM
- **Active Directory domain:** `johnson.local`
- **Directory services:** Active Directory Domain Services (AD DS) and DNS
- **Client VM:** Windows 11 is available in the lab environment for client-side testing

## Work Covered

- Domain controller and Active Directory administration
- Organizational Units and test user accounts
- Global security groups for role-based organization
- Group Policy configuration and policy refresh/verification
- Desktop personalization, Control Panel, and removable-storage restrictions
- Password policy exploration
- Drive mapping through Group Policy
- Basic account, DNS, network, and Windows service troubleshooting

## Documentation

1. [Lab setup](documentation/01-lab-setup.md)
2. [Domain controller](documentation/02-domain-controller.md)
3. [User management](documentation/03-user-management.md)
4. [Security groups](documentation/04-security-groups.md)
5. [Group Policy management](documentation/05-group-policy-management.md)
6. [Troubleshooting](documentation/06-troubleshooting.md)

Screenshots documenting selected configuration steps are stored in the [screenshots folder](screenshots/).

> This is an isolated learning environment using fictional accounts. Policy behavior and domain-join results should be described as verified only after testing them on a client VM.
