# Group Policy Management

## Overview

Group Policy Management was used to explore centralized configuration of Windows user and computer settings in the Active Directory lab. The exercises included desktop restrictions, Control Panel access, removable-storage policy, password-policy settings, and drive mapping.

## Policies Explored

### Desktop Wallpaper

Created a GPO named **Desktop Wallpapers** to explore preventing a user from changing the desktop wallpaper.

Evidence: [View GPO policy list](../screenshots/GPO-Policies-Created.png)

### Control Panel Restrictions

Created a GPO named **Restrict control panel** to explore limiting access to Control Panel.

Evidence: [View Control Panel policy screenshot](../screenshots/GPO-control-panel.png)

### Removable Storage

Explored policies for restricting access to removable storage devices. Such restrictions can help reduce unauthorized data transfer when correctly scoped and tested.

Evidence:
- [View removable-storage policy](../screenshots/GPO-Restricting-Storage-Devices.png)
- [View storage-device settings](../screenshots/GPO-Storage-Devices.png)

### Password Policy

Reviewed password policy settings after a test user password was rejected. The exercise involved checking minimum password length and complexity requirements. Password policy settings should be verified in the domain-level policy and checked against the effective domain settings.

Evidence:
- [View password policy screenshot](../screenshots/password-policies.png)
- [View password requirements screenshot](../screenshots/group-policy-password-requirements.png)

### Drive Mapping

Created a drive-mapping policy to map a user storage location to drive letter `E:`. The mapping depends on the configured target path and policy scope; verify it from a client session before claiming client-side success.

Evidence: [View drive-mapping screenshot](../screenshots/drive-mapping1.png)

## Policy Refresh and Verification

Commands used for policy refresh and account-policy review:

```cmd
gpupdate /force
net accounts /domain
```

- `gpupdate /force` requests a Group Policy refresh on the computer where it is run.
- `net accounts /domain` displays domain account policy information.

Evidence: [View policy refresh/check screenshot](../screenshots/update-check-policies.png)

A refresh command alone does not prove that every policy applied successfully. Validate the relevant setting on the target user or computer, and inspect policy results when needed.

## Troubleshooting Notes

During test-account creation, a password was rejected. Group Policy Management was used to investigate password requirements. The experience reinforced the need to distinguish the policy being edited from the policy that actually governs domain users.

## Best Practice

- Link GPOs to the intended domain or OU.
- Use clear names that describe the policy's purpose.
- Keep policy scope narrow enough to avoid unintended impact.
- Test restrictions using a non-administrative lab account.
- Record the setting, scope, test result, and any limitations.
