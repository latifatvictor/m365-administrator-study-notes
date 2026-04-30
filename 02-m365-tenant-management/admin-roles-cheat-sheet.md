# Microsoft 365 Administrator Roles Cheat Sheet

---

## 🔑 Key Points

- Microsoft 365 uses RBAC: Role-Based Access Control
- Roles give users permission to perform admin tasks
- Always follow least privilege
- Avoid giving Global Admin unless truly needed

---

## 🔐 Security Best Practices

- Keep Global Admins limited to 2-4 people
- Require MFA for all admins
- Use the least permissive role
- Use Global Reader for read-only audits
- Use PIM for temporary admin access where possible

---

## 👤 Common Admin Roles

| Role | Main Use |
|---|---|
| Global Administrator | Full access across Microsoft 365 |
| Global Reader | Read-only access across Microsoft 365 |
| User Administrator | Manage users, groups, licences, passwords |
| Helpdesk Administrator | Reset passwords, force sign-out, support users |
| Password Administrator | Reset passwords for limited users |
| Exchange Administrator | Manage mailboxes, mail flow, shared mailboxes |
| SharePoint Administrator | Manage SharePoint and OneDrive |
| Teams Administrator | Manage Teams, meetings, messaging, voice |
| Security Administrator | Manage security alerts, policies, threats |
| Compliance Administrator | Manage compliance, eDiscovery, DLP |
| Billing Administrator | Manage subscriptions and billing |
| Licence Administrator | Manage user and group licence assignments |
| Groups Administrator | Manage Microsoft 365 groups and policies |
| Reports Reader | View usage, audit, sign-in and activity reports |
| Message Center Reader | View service updates and advisory messages |
| Service Support Administrator | Manage support requests and service health |
| Power Platform Administrator | Manage Power Apps, Power Automate and DLP |
| Office Apps Administrator | Manage Microsoft 365 Apps policies and settings |

---

## 💼 Real Work Scenarios

- Helpdesk staff → Helpdesk Administrator
- IT support analyst → User Administrator
- Exchange engineer → Exchange Administrator
- Security analyst → Security Administrator
- Compliance officer → Compliance Administrator
- Finance team → Billing Administrator
- Auditor → Global Reader or Reports Reader
- Teams engineer → Teams Administrator
- SharePoint owner/admin → SharePoint Administrator

---

## ⚠️ Common Mistakes

- Giving Global Admin to too many users
- Not enabling MFA for admin accounts
- Using Global Admin when a limited role is enough
- Not reviewing admin role assignments regularly
- Forgetting that some services have separate admin roles

---

## 🔥 Interview Questions

### Q1: What is RBAC in Microsoft 365?
RBAC means Role-Based Access Control. It allows admins to assign predefined roles instead of assigning individual permissions manually.

---

### Q2: Why should Global Admin be limited?
Because Global Admin has almost full control across Microsoft 365, making it a high-risk role if compromised.

---

### Q3: What role should be used for someone who only needs to view settings?
Global Reader.

---

### Q4: What role is best for password resets?
Helpdesk Administrator or Password Administrator, depending on the level of access needed.

---

### Q5: What role manages mailboxes and mail flow?
Exchange Administrator.

---

### Q6: What role manages Teams settings?
Teams Administrator.

---

### Q7: What role manages DLP, eDiscovery and compliance?
Compliance Administrator.

---

### Q8: What role manages security alerts and threats?
Security Administrator.

---

### Q9: What is the principle of least privilege?
Giving users only the permissions they need to do their job.

---

### Q10: Why is MFA important for admins?
Because admin accounts have sensitive access, and MFA protects them if passwords are compromised.

---

## 🧠 Summary

- Roles control admin permissions
- Global Admin should be tightly controlled
- Use least privilege
- Match roles to job responsibilities
- Review admin access regularly
