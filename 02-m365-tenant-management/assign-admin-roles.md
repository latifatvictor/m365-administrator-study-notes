# Microsoft 365 Admin Roles – Complete Guide (MS-102)

---

## 🔑 Core Concepts

- Microsoft 365 uses RBAC (Role-Based Access Control)
- Roles = collection of permissions
- Assign roles instead of individual permissions
- One user can have multiple roles
- Always follow least privilege

---

## 🧠 Where Roles Are Managed

1. Microsoft 365 Admin Center
   - Main portal
   - Manage users, roles, licences

2. Microsoft Entra ID
   - Identity & access management
   - Conditional Access, PIM

3. Microsoft Defender Portal
   - Security roles
   - Threat detection & response

4. Microsoft Purview
   - Compliance roles
   - DLP, eDiscovery

---

## ⚠️ Key Rule

Same role name does NOT always mean same permissions across portals

Example:
- Exchange Admin (M365) → basic tasks
- Exchange Admin (Exchange portal) → advanced tasks

---

## 👤 Common Admin Roles

- Global Administrator → Full access
- Global Reader → Read-only
- User Administrator → Manage users & licences
- Helpdesk Administrator → Reset passwords
- Exchange Administrator → Manage mailboxes
- SharePoint Administrator → Manage SharePoint
- Teams Administrator → Manage Teams
- Security Administrator → Security policies & alerts
- Compliance Administrator → Compliance & eDiscovery
- Billing Administrator → Billing & subscriptions
- Licence Administrator → Assign licences
- Groups Administrator → Manage groups
- Reports Reader → View reports
- Service Support Admin → Support tickets

---

## 💼 Real Work Scenarios

- Helpdesk → Helpdesk Admin
- IT Support → User Admin
- Exchange Engineer → Exchange Admin
- Security Analyst → Security Admin
- Auditor → Global Reader

---

## 🔐 Best Practices

1. Least Privilege
- Only give required permissions

Example:
Use Helpdesk Admin instead of Global Admin

---

2. Use PIM (Just-In-Time Access)
- Temporary admin access
- Auto removed after use

---

3. Enforce MFA
- Required for all admins

---

4. Run Access Reviews
- Remove unused access

---

5. Limit Global Admins
- Keep between 2–4

---

6. Use Role Groups
- Assign roles to groups, not individuals

---

7. Use Cloud-Only Admin Accounts
- Avoid on-prem synced admin accounts

---

## ⚡ Assigning Admin Roles

### Method 1: Admin Center

Steps:
1. Go to Microsoft 365 Admin Center
2. Users → Active Users
3. Select user
4. Manage roles
5. Assign role
6. Save

---


---

## 🔄 Role Assignment Rules

- Entra roles → Users + role groups
- Exchange roles → Users + mail-enabled groups
- Intune roles → Security groups

---

## ⚠️ Common Mistakes

- Too many Global Admins
- No MFA on admin accounts
- Assigning wrong roles
- Not using role groups
- No access reviews
- Permanent high-level access

---

## 🔥 Interview Questions

Q1: What is RBAC?
Role-Based Access Control – assigning roles instead of permissions

---

Q2: Why limit Global Admins?
They have full access → high risk

---

Q3: What is least privilege?
Giving only required access

---

Q4: What is PIM?
Privileged Identity Management → temporary admin access

---

Q5: How do you assign roles?
Admin Center or PowerShell

---

Q6: Can a user have multiple roles?
Yes

---

Q7: Why use role groups?
Easier management

---

Q8: Why MFA for admins?
Protects against compromised passwords

---

Q9: Why might a role not appear in PowerShell?
Not activated

---

Q10: Difference between M365 role and service role?
M365 = broad
Service = granular

---

## 🧠 Final Summary

- Roles control access in Microsoft 365
- Always use least privilege
- Use PIM for temporary access
- Limit Global Admins
- Use groups for scalability
- Review access regularly

---

## 🚀 Strong Interview Answer

If asked:

“How do you manage admin roles in Microsoft 365?”

Answer:

I assign roles using the Microsoft 365 admin center and Microsoft Graph PowerShell. I follow least privilege, use PIM for just-in-time access, enforce MFA for all admins, limit Global Administrators, and regularly review access.
