# Active Directory Troubleshooting

## Purpose

This document records troubleshooting methods practiced or prepared for the Windows Server Active Directory lab. Record the actual command output and outcome for each test performed; do not mark a check as passed without evidence.

## 1. User Account Issues

**Scenario:** A test user cannot sign in.

1. Open Active Directory Users and Computers.
2. Locate the account in the `Employees` OU.
3. Check whether the account is enabled and inspect account properties.
4. If the account was intentionally disabled for the lab exercise, re-enable it.
5. If the password may be incorrect or expired, follow the password-reset workflow and test again.

**Relevant skills:** account-status checks, account enable/disable, password-reset workflow, OU navigation.

## 2. Group Policy

Run the following from an elevated Command Prompt:

```cmd
gpupdate /force
gpresult /r
net accounts /domain
```

- `gpupdate /force` requests a policy refresh.
- `gpresult /r` reports applied Group Policy information for the computer and current user context.
- `net accounts /domain` displays domain account policy settings.

A successful refresh does not prove that every setting applied. Check the relevant user/computer scope and verify the setting on the target system.

## 3. Network Connectivity

```cmd
ipconfig /all
ping 127.0.0.1
ping 192.168.122.1
```

- `ipconfig /all` displays IP configuration, DNS servers, and adapter details.
- `ping 127.0.0.1` tests the local TCP/IP loopback.
- `ping 192.168.122.1` tests the common libvirt NAT gateway address; confirm the actual gateway with `ipconfig` because the address can differ.

If connectivity fails, confirm the adapter is connected, check the IP address and subnet, and verify the correct gateway before changing settings.

## 4. DNS and Active Directory Discovery

```cmd
nslookup johnson.local
nslookup -type=SRV _ldap._tcp.dc._msdcs.johnson.local
dcdiag /test:dns
```

These commands check domain name resolution, Active Directory LDAP service records, and DNS-related domain-controller diagnostics. Review the configured DNS server in `ipconfig /all`; domain clients should use DNS that can resolve the Active Directory domain.

## 5. Windows Services

```cmd
sc query DNS
sc query NTDS
sc query Netlogon
```

These commands inspect the state of the DNS Server, Active Directory Domain Services, and Netlogon services. Investigate service state and relevant logs before attempting a restart or configuration change.

## 6. Domain Controller Health

```cmd
dcdiag /v
```

Review the diagnostic output for failed tests and errors. Capture the relevant failure and investigate its cause rather than recording the test as successful by default.

## Troubleshooting Workflow

1. Define the symptom and scope.
2. Check account status, network configuration, DNS, or service state as appropriate.
3. Run a targeted diagnostic.
4. Record the exact error or result.
5. Make one controlled change at a time.
6. Repeat the original test to verify the outcome.
7. Document the cause, resolution, and remaining limitations.

## Evidence and Results

Attach screenshots or command output after each test is actually performed. This document is a runbook; update it with confirmed results as the lab is tested.
