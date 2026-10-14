# Domain Controller Setup

## Overview

A Windows Server 2025 virtual machine was configured as the domain controller for the lab Active Directory environment.

## Environment

- **Operating system:** Windows Server 2025 Evaluation
- **Virtualization:** QEMU/KVM on Ubuntu
- **Domain:** `johnson.local`
- **Network:** libvirt virtual network using NAT
- **Intended server hostname:** `DT-DC01` (confirm the hostname on the VM before relying on it)

## Configuration

1. Installed the Active Directory Domain Services role.
2. Promoted the server to a domain controller and created the lab domain/forest.
3. Used DNS as part of the Active Directory environment so domain clients can locate directory services.
4. Opened Active Directory Users and Computers and Group Policy Management to administer directory objects and policies.

## Validation Checklist

Use this checklist to record verified results rather than assuming the configuration is healthy.

- [ ] Confirm the computer hostname with `hostname`.
- [ ] Confirm the domain with `systeminfo` or the server's domain properties.
- [ ] Confirm Active Directory Users and Computers opens and displays `johnson.local`.
- [ ] Confirm the DNS Server service is running with `sc query DNS`.
- [ ] Check domain-controller health with `dcdiag /v`.
- [ ] Test DNS service records with `nslookup -type=SRV _ldap._tcp.dc._msdcs.johnson.local`.
- [ ] Join the Windows 11 VM to the domain and test a domain-user sign-in, if not already completed.

## Evidence

[View the domain name screenshot](../screenshots/active-directory-name-screenshot.png)

## Notes

The domain name in the screenshots and the live VM should be treated as the source of truth. Keep this document aligned with the actual VM configuration if the hostname or domain is changed.
