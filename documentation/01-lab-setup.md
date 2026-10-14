# Lab Setup

## Objective

Build an isolated Windows Server lab to practice common systems administration and IT support tasks for a fictional business environment.

## Environment

| Component | Configuration |
|---|---|
| Host operating system | Ubuntu |
| Hypervisor | QEMU/KVM with Virtual Machine Manager |
| Server VM | Windows Server 2025 Evaluation |
| Client VM | Windows 11 |
| Active Directory domain | `johnson.local` |
| Virtual networking | libvirt virtual network / NAT |

## Lab Goals

- Deploy Active Directory Domain Services (AD DS).
- Use DNS to support Active Directory name and service discovery.
- Organize directory objects with Organizational Units (OUs).
- Create and maintain test user accounts.
- Create security groups for role-based organization.
- Configure and review Group Policy Objects (GPOs).
- Practice password-policy investigation and policy refresh.
- Explore drive mapping and workstation restrictions through Group Policy.
- Use Windows command-line tools to inspect network settings, DNS, services, and domain-controller health.

## Scope and Safety

The environment uses fictional users and is intended for learning. Restrictive policies should be tested in the lab before being considered for production use. A successful configuration should be supported by a screenshot, command output, or client-side test where applicable.

## Evidence

Screenshots are maintained separately in the [screenshots directory](../screenshots/). Individual procedure documents link to relevant evidence.
