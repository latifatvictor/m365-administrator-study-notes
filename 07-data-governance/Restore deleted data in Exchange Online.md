## Restore Deleted Data in Exchange Online Summary

### Overview:
Restoring deleted email data in Exchange Online is a **two-step process**:
1. **Recover deleted items** → into a discovery mailbox  
2. **Restore recovered items** → back to the original mailbox  

---

## Deletion Types:

### 1. Soft Deletion
- Item moved to: **Recoverable Items → Deletions**
- Default retention:
  - **14 days** (extendable up to 30 days)
- Users can recover items via:
  - Outlook / Outlook on the web

---

### 2. Hard Deletion (Purge)
- Permanently deleted by user (Shift+Delete or purge)
- Stored in: **Recoverable Items → Purges**
- Still recoverable by admins if:
  - Retention period not expired
  - **Single item recovery enabled** (default)

---

## Step 1: Recover Deleted Items

### Requirements:
- Source mailbox  
- Target mailbox (**discovery mailbox**)  
- Search criteria (subject, sender, date, etc.)  

---

### Method 1: Exchange Admin Center (EAC)
1. Go to **Recipients → Mailboxes**
2. Select mailbox
3. Choose **Recover deleted items**
4. Apply filters
5. Recover to discovery mailbox

---

### Method 2: PowerShell
```powershell
Get-RecoverableItems -Identity laura@contoso.com `
-SubjectContains "FY17 Accounting" `
-FilterItemType IPM.Note `
-FilterStartTime "2/1/2023 12:00:00 AM" `
-FilterEndTime "2/5/2023 11:59:59 PM"
``
