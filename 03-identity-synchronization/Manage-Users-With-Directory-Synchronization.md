# Manage Users with Directory Synchronization

## Overview
Organizations using directory synchronization must perform several management and maintenance tasks to ensure:
- Users synchronize correctly
- Synchronization services remain healthy
- User accounts remain manageable
- Password and device writeback features function properly

This guide covers:
- Managing synchronized user accounts
- Recovering deleted users
- Recovering orphaned objects
- Password writeback
- Device writeback
- Enhanced user management

---

# Managing User Accounts

Administrators can manage synchronized users using:
- Active Directory Users and Computers
- Windows PowerShell in on-premises Active Directory

Administrators cannot manage synchronized user accounts directly from:
- Microsoft 365 admin center
- Exchange Online admin center (EAC)

## Source of Authority
After synchronization:
- On-premises Active Directory becomes the source of authority
- Changes made in Microsoft 365 admin center are not written back to on-premises AD

---

# Attributes Managed in Microsoft 365

Some attributes are cloud-only and must be managed in Microsoft 365:

Examples include:
- Microsoft 365 licenses
- Exchange Online In-place Archiving settings

---

# Recovering Accidentally Deleted User Accounts

Microsoft Entra ID supports soft delete functionality.

## Scenario
If:
- A user is deleted from on-premises AD
- Synchronization occurs

Then:
- The user becomes deleted in Microsoft Entra ID
- The account disappears from Active users
- Licenses become available for reassignment

## Recovery Period
Deleted users can be restored within:
- 30 days

---

# Restore Deleted User via Microsoft 365 Admin Center

## Steps
1. Open Microsoft 365 admin center
2. Select Users
3. Select Deleted users
4. Select the deleted user
5. Select Restore user

## Password Options
Administrators can:
- Autogenerate password
- Manually create password

If Password Hash Synchronization is enabled:
- Next synchronization overwrites the temporary password

---

# Restore Deleted User Using PowerShell

## Microsoft Graph PowerShell Cmdlet

```powershell
Restore-MgDirectoryDeletedItem
