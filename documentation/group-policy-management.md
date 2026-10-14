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


## Troubleshooting

- While creating a test user account, I encountered an error and had to change the domain password requirements. 
- Navigated to the Password Policy settings in Group Policy Management to investigate the requirements and identify a solution.
- Created temporary password requirements [shown here](../screenshots/group-policy-password-requirements.png)
