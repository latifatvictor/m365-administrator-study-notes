# Create and Manage Groups in Microsoft 365

---

## 🔑 Overview

Groups in Microsoft 365 are essential for:

- managing access to resources
- assigning permissions
- enabling collaboration
- simplifying administration

Instead of assigning permissions to individual users, organisations should use groups.

---

## 🧠 Real-World Example

A company creates a **Security Group for Marketing users** and grants that group access to a SharePoint site.

👉 Result:
- Easy access management
- No need to manage users individually

---

## ✅ Best Practices

- Use **clear and simple naming conventions**
- Define **group governance policies**
- Assign **permissions to groups, not users**
- Maintain a **consistent provisioning process**
- Always assign **at least 2 group owners**

---

## 🛠️ Create a Group (Admin Center)

1. Go to **Microsoft 365 Admin Center**
2. Select:
   - Groups → Active groups
3. Click **Add a group**
4. Select **Group type**
5. Enter:
   - Name
   - Description
6. Assign **Owners**
7. Configure:
   - Email (if applicable)
   - Privacy (Public / Private)
   - Teams (optional)
8. Review and click **Create**

---

## ⚠️ Important

- Synced groups from on-prem AD **cannot be edited in M365**. You can only use local Active Directory management tools to modify security groups that are synchronized with your on-premises Active Directory.
- Must use **on-prem Active Directory tools**

---

## 💻 Create Group with PowerShell

```powershell
New-MgGroup -DisplayName "Test Group" `
-MailEnabled:$False `
-MailNickName "testgroup" `
-SecurityEnabled
