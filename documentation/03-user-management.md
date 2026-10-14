# Active Directory User Management

## Objective

Practice creating and organizing user accounts in Active Directory Users and Computers (ADUC), using Organizational Units (OUs) to keep directory objects organized.

## Organizational Units

The lab includes or planned the following OUs:

- **Employees** — test employee accounts
- **Computers** — intended location for computer objects
- **Security Groups** — intended location for security groups

Verify the final OU list in ADUC before describing every OU as configured.

## Test Accounts

Three fictional accounts were created for administration practice:

| Name | Logon name | Intended lab role |
|---|---|---|
| Alex Morgan | `amorgan` | IT Support |
| Sarah Chen | `schen` | Office Staff |
| David Wilson | `dwilson` | Production |

[View the user accounts screenshot](../screenshots/users-created.png)

## Account Administration Skills

The lab exercises focus on:

- Creating user objects in the appropriate OU
- Setting initial passwords in line with the domain's current password policy
- Reviewing account properties and account status
- Practicing password-reset workflows
- Enabling or disabling a test account for troubleshooting, then restoring its normal state

## Password Creation Issue

During creation of the Alex Morgan account, Windows rejected the initial password. The Password Policy section of Group Policy Management was reviewed to understand the configured minimum length and complexity requirements. This exercise highlighted the importance of checking the effective domain password policy before troubleshooting account creation.

[View password policy settings screenshot](../screenshots/group-policy-password-requirements.png)

## Administrative Note

Use only lab passwords for these fictional accounts. Do not store passwords in this repository. If an account is disabled during a troubleshooting exercise, re-enable it and confirm its status before ending the lab session.
