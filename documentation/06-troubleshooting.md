# Active Directory Troubleshooting

## Overview

This document records troubleshooting exercises performed in a Windows Server Active Directory lab. The exercises focus on user account management, Group Policy, network connectivity, DNS, and Windows services.

## 1. User Account Troubleshooting

### Scenario
A user cannot sign in to their domain account.

### Troubleshooting Steps
1. Opened Active Directory Users and Computers.
2. Located the user in the Employees organizational unit.
3. Checked the user's account status.
4. Practiced disabling and re-enabling a test account to understand account administration.

### Resolution
Re-enabled the test account after the exercise.

### Skills Practiced
- Checking Active Directory account status
- Enabling and disabling user accounts
- Navigating organizational units
- Basic account troubleshooting

## 2. Group Policy Verification

### Objective
Check domain account policy settings and refresh Group Policy.

### Commands
```cmd
gpupdate /force
net accounts /domain
