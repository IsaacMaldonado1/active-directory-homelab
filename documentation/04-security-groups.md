# Active Directory Security Groups

## Objective

Use security groups to organize users by role. In a business environment, permissions are normally assigned to groups rather than configured individually for each user.

## Group Configuration

The lab uses Global Security groups under the `Security Groups` OU.

| Group | Intended purpose | Intended member |
|---|---|---|
| `IT Support` | Organize users performing support tasks | Alex Morgan (`amorgan`) |
| `Office Staff` | Represent office/administrative users | Sarah Chen (`schen`) |
| `Production` | Represent production users | David Wilson (`dwilson`) |

[View IT Support group screenshot](../screenshots/active-directory-IT-support-group.png)

## Verification

For each group, open **Properties → Members** in Active Directory Users and Computers and confirm that membership matches the table. If the groups have not all been created or membership has not been updated yet, complete those steps before treating the table as the verified final state.

## Why Groups Matter

- Simplify administration when roles change.
- Provide a central place to manage membership.
- Support role-based access control when permissions are assigned to the group.
- Reduce the need to assign the same resource permissions separately to each user.

**Important:** Creating a security group does not automatically grant permissions or administrative rights. Access must be explicitly assigned to resources or delegated through appropriate administrative mechanisms.
