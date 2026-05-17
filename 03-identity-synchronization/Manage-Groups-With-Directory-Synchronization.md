# Manage Groups with Directory Synchronization

## Overview

Once an organization implements directory synchronization between its on-premises Active Directory (AD) and Microsoft Entra ID, all group membership management must occur in the on-premises Active Directory.

Organizations can use either:
- Microsoft Entra Connect Sync
- Microsoft Entra Cloud Sync

to synchronize groups and memberships between on-premises AD and Microsoft Entra ID.

After synchronization is enabled:
- The source of authority for groups and memberships becomes the on-premises Active Directory.

---

# Group Synchronization

Directory synchronization synchronizes:
- Groups
- Group memberships

from:
- On-premises Active Directory

to:
- Microsoft Entra ID

This process behaves similarly to user synchronization.

---

# Group Writeback

Group writeback is a feature that writes Microsoft 365 groups from Microsoft Entra ID back to the on-premises Active Directory.

This feature allows:
- Microsoft 365 groups created in the cloud
- To appear on-premises as distribution groups

---

# Group Writeback in Microsoft Entra Connect Sync

Group writeback is an optional feature in Microsoft Entra Connect Sync.

---

# Requirements for Group Writeback

Organizations must complete the following prerequisites:

- Exchange Server 2013 CU8 or later
OR
- Exchange Server 2016 or later

---

# Prepare Active Directory

Administrators must:
- Create the required Organizational Unit (OU)
- Configure appropriate permissions

Microsoft Entra Connect Sync provides the following built-in PowerShell cmdlet to automate preparation:

```powershell
Initialize-ADSyncGroupWriteBack
