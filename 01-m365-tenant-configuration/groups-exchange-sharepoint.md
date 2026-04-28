# Create Groups in Exchange Online & SharePoint (Quick Notes)

---

## 🔑 Key Points

- Groups can be created in:
  - Microsoft 365 admin center
  - Exchange Online
  - SharePoint Online

---

## 📧 Groups in Exchange Online

### Purpose
- Primarily for **email communication + access management**

### Group Types

1. **Microsoft 365 Group**
   - Collaboration (email, files, calendar, Teams)
   - Best for teamwork

2. **Distribution Group**
   - Email only (broadcast messages)
   - No permissions

3. **Mail-enabled Security Group**
   - Email + permissions
   - Used for SharePoint/OneDrive access

4. **Dynamic Distribution Group**
   - Auto-updated membership (based on rules)
   - Email only

---

## ⚠️ Important Notes (Exchange)

- Created in Exchange → visible in M365 admin center
- Can delete in both places
- Can only edit in Exchange admin center
- Dynamic groups do NOT show in Security groups page

---

## 🌐 Groups in SharePoint Online

### Purpose
- Manage **site-level permissions**

### Default Groups (Auto-created)

- Visitors → Read access
- Members → Edit access
- Owners → Full control

---

## 🧠 Key Concept

SharePoint Groups:
- Used ONLY within SharePoint
- Control access to:
  - Sites
  - Libraries
  - Lists

---

## 🔄 Best Practice

👉 Use Microsoft Entra Security Groups inside SharePoint  
Instead of adding users individually

Why?
- Easier management
- Scalable
- Central control

---

## 🔐 Security Group vs SharePoint Group

| Feature | Security Group | SharePoint Group |
|--------|--------------|-----------------|
| Scope | Tenant-wide | SharePoint only |
| Use | Permissions across M365 | Site-level access |
| Email | Only if mail-enabled | No |

---

## 💼 Real Work Scenarios

- Create **Distribution group** for company-wide emails
- Use **Mail-enabled security group** for:
  - Granting SharePoint access + sending emails
- Use **M365 group** for:
  - Teams collaboration
- Use **SharePoint groups** for:
  - Managing site permissions (Owners, Members, Visitors)

---

## 🎯 Why It Matters (In Real Jobs)

- Controls access across systems
- Reduces admin workload
- Improves security & governance
- Essential for Teams + SharePoint management

---

## 🔥 Interview Questions

Q1: What group types can you create in Exchange Online?
A: M365 groups, Distribution groups, Mail-enabled security groups, Dynamic distribution groups

Q2: What is the difference between a distribution group and M365 group?
A: Distribution = email only, M365 = collaboration + resources

Q3: What is a mail-enabled security group?
A: A group used for both permissions and email

Q4: What is the difference between SharePoint groups and security groups?
A: SharePoint groups are site-specific, security groups are tenant-wide

Q5: Can you email a security group?
A: Only if it is mail-enabled

---

## 🧠 Summary

- Exchange groups = email + access control
- SharePoint groups = site permissions
- Use security groups for scalability
- Choose group type based on use case
