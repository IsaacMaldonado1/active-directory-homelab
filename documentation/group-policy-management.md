screenshots/group-policy-password-requirements.png

# Group Policy Management

## Overview
I used Group Policy Management to investigate domain password requirements in my Active Directory lab.

## Domain Password Policy
- Configured the Default Domain Policy to strengthen password security.
- Password history: 5 passwords
- Maximum password age: 90 days
- Minimum password length: 8 characters
- Password complexity: Enabled
- [View password policies here!](../screenshots/password-policy.png)

## Policy Verification

Refreshed Group Policy and checked the effective domain account settings.

The commands and the outputs can be found [here!](../screenshots/update-check-policies.png)
- Command: `gpupdate /force`
- Verification: `net accounts /domain`

This verified the domain's account policy configuration.

## drive mapping

Made a new drive map for user storage. Assigned it to local drive letter E. 
Can be found 


## Troubleshooting

- While creating a test user account, I encountered an error and had to change the domain password requirements. 
- Navigated to the Password Policy settings in Group Policy Management to investigate the requirements and identify a solution.
- Created temporary password requirements [shown here](../screenshots/group-policy-password-requirements.png)
