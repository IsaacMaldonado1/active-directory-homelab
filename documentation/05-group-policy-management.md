# Group Policy Management

## Overview
I used Group Policy Management to investigate domain password requirements, restrict access to desktop wallpapers, control panels, and USB devices. 
All of the Group policies that I made can be found [here!](../screenshots/GPO-Policies-Created)


## Restrictions made

Wallpapers 
- Made a GPO called "Desktop Wallpapers" and learned how to restrict a user from changing their wallpaper.
- Screenshot of the activity: [Wallpaper GPO.](../screenshots/GPO-Wallpaper.png)

Control Panel Access
- Made a GPO called "Restrict control panel" and learned how to restrict a user from being able to access their control panel.
- Screenshot of the activity: [Control Panel Access GPO.](../screenshots/GPO-control-panel.png)

Password Policies
- Made a GPO called "Password policies" and learned how to configure password policies.
- Screenshot of the activity: [Password Policies GPO](../screenshots/password-policy.png)

## Drive Mapping

- Made a new drive map for user storage. Assigned it to local drive letter E. 
- Screenshot of the activity: [Drive Mapping GPO](../screenshots/drive-mapping1.png)

## Policy Verification

After every policy made I refreshed Group Policy and checked the effective domain account settings.

The commands and the outputs can be found [here!](../screenshots/update-check-policies.png)
- Command: `gpupdate /force`
- Verification: `net accounts /domain`
- This verified the domain's account policy configuration.



## Troubleshooting

- While creating a test user account, I encountered an error and had to change the domain password requirements. 
- Navigated to the Password Policy settings in Group Policy Management to investigate the requirements and identify a solution.
- Created temporary password requirements [shown here](../screenshots/group-policy-password-requirements.png)
