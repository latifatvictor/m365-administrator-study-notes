## Enable Archive Mailboxes in Microsoft 365 Summary

### Overview:
- Archive mailboxes provide **additional storage** and support **compliance practices**
- Can be:
  - Enabled via **Exchange Admin Center (EAC)**
  - Enabled via **PowerShell**
- Requires appropriate permissions (Mail Recipients role)

---

## Prerequisites:
- User must have:
  - **Mail Recipients role**
- Default roles that include this:
  - Recipient Management  
  - Organization Management  

---

## Enable Archive Mailbox (EAC Steps):
1. Go to **Microsoft 365 admin center → Exchange**
2. Select **Manage mailboxes**
3. Choose the user
4. Open **Others tab**
5. Select **Manage mailbox archive**
6. Toggle **Mailbox archive → Enabled**
7. Save

✅ Result:
- Archive mailbox created
- Status shown as **Active**

---

## Disable Archive Mailbox:
- Same steps as enabling
- Toggle **Mailbox archive → Disabled**

⚠️ Important:
- Data recoverable for **30 days**
- After 30 days → permanently deleted
- Re-enabling after 30 days creates a **new archive mailbox**

---

## Default Archiving Behavior:
- Emails:
  - Moved after **2 years**
- Based on:
  - **Default retention policy**

---

## PowerShell Commands:

### Enable (Single User):
```powershell
Enable-Mailbox -Identity <username> -Archive
