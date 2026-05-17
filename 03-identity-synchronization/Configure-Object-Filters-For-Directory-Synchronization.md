# Suggested File Name
Configure-Object-Filters-For-Directory-Synchronization.md

# Configure Object Filters for Directory Synchronization

## Overview

Object filtering is a directory synchronization feature that controls which objects synchronize from on-premises Active Directory to Microsoft Entra ID.

Filtering is considered an advanced configuration topic because it allows organizations to customize synchronization behavior to meet specific business, compliance, pilot, or operational requirements.

Object filtering allows organizations to customize directory synchronization between on-premises Active Directory and Microsoft Entra ID. Supported filtering methods include group-based, domain-based, OU-based, and attribute-based filtering. Microsoft Entra Connect Sync supports all filtering types, while Microsoft Entra Cloud Sync currently supports group, domain, and OU filtering only. Because filtering can remove synchronized objects from Microsoft Entra ID, administrators should carefully validate all filtering configurations before exporting changes.

By default:
- Microsoft Entra Connect Sync synchronizes all supported objects from all configured domains and forests.

Microsoft recommends using the default configuration whenever possible because it provides:
- A complete Global Address List (GAL)
- Better collaboration experience
- Consistent Microsoft 365 communication experience

This setup closely matches traditional on-premises Exchange Server or Skype for Business environments.

---

# Reasons for Using Object Filtering

Organizations may need filtering for several reasons:

- Pilot deployments where only selected users should synchronize
- Excluding service accounts or nonpersonal accounts
- Compliance requirements
- Excluding disabled accounts from Microsoft Entra ID
- Limiting synchronization scope
- Reducing unnecessary cloud objects

---

# Types of Filtering

Microsoft Entra directory synchronization supports several filtering methods.

---

# Group-Based Filtering

Group-based filtering synchronizes objects based on membership in a specific group.

## Characteristics

- Must be configured during initial installation
- Provides granular control
- Easy to manage
- Reduces synchronization traffic

## Limitations

- Limited filtering flexibility
- Potential setup errors
- Large groups may slow synchronization cycles

---

# Domain-Based Filtering

Domain-based filtering allows administrators to:
- Select which domains synchronize to Microsoft Entra ID

Administrators can:
- Add domains
- Remove domains
- Adjust synchronization scope as infrastructure changes

---

# Organizational Unit (OU)-Based Filtering

OU-based filtering synchronizes only selected Organizational Units.

## Benefits

- Simple structure-based filtering
- Useful for pilots
- Easy delegation

## Applies To

- Users
- Groups
- Contacts
- Other object types inside selected OUs

---

# Object Attribute-Based Filtering

Attribute-based filtering synchronizes objects based on specific attribute values.

## Examples

- Department
- Employee type
- Custom attributes
- Account status

## Important

Attribute-based filtering:
- Is ONLY supported in Microsoft Entra Connect Sync
- Is NOT supported in Microsoft Entra Cloud Sync

---

# Combining Multiple Filters

Organizations can combine multiple filtering methods.

## Example

An organization may:
- Synchronize only one OU
AND
- Further filter users based on attributes

## Logic Used

Multiple filters use:
- Logical AND

This means:
- Objects must satisfy all filtering conditions

---

# Filtering Support Comparison

| Filtering Type | Microsoft Entra Connect Sync | Microsoft Entra Cloud Sync |
|---|---|---|
| Group-Based Filtering | Supported | Supported |
| Domain-Based Filtering | Supported | Supported |
| OU-Based Filtering | Supported | Supported |
| Attribute-Based Filtering | Supported | Not Supported |

---

# Important Behavior of Filtering

When filtering is enabled after synchronization has already occurred:

- Previously synchronized objects that no longer meet filtering requirements are removed from Microsoft Entra ID

This behavior can result in:
- Large object deletions

---

# Filtering Configuration Retention

When:
- Upgrading Microsoft Entra Connect Sync

The filtering configuration is:
- Retained automatically

## Best Practice

Always verify:
- Filtering settings after upgrades

before:
- Running the next synchronization cycle

---

# Multi-Forest Considerations

If an organization uses:
- Multiple forests

Then:
- Filtering configuration must be applied separately to each forest

if consistent filtering is required.

---

# Prevent Accidental Deletes

Microsoft Entra Connect Sync includes:
- Prevent accidental deletes feature

This feature is:
- Enabled by default

---

# Default Delete Threshold

Default protection threshold:
- 500 objects

If more than 500 deletions occur:
- Synchronization export stops
- Administrator review is required

---

# Recovering Deleted User Objects

If users are accidentally filtered out:

Administrators can:
- Remove the filtering rule
- Resynchronize directories

This action restores:
- User objects from Microsoft Entra recycle bin

---

# Important Limitation

## Non-User Objects

Some object types cannot be recovered automatically.

Example:
- Security groups
- Access control lists (ACLs)

If deleted accidentally:
- Permissions may be permanently lost

---

# Disable the Synchronization Scheduler Before Changes

Before modifying filtering configuration:

Administrators should disable:
- Automatic synchronization scheduler

This prevents:
- Accidental exports before verification

---

# Disable Synchronization Scheduler

## PowerShell Command

```powershell
Set-ADSyncScheduler -SyncCycleEnabled $False
