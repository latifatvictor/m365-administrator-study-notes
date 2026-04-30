# Microsoft 365 Role Groups & Delegated Administration (MS-102)

---

## 🧩 Role Groups – Key Points

- Role groups = assign roles to a group instead of users
- Users inherit permissions via group membership
- Supports built-in and custom roles
- Improves scalability and consistency

---

## 🎯 Why Use Role Groups

- Simplifies role assignment
- Ensures consistent permissions
- Easier onboarding/offboarding
- Improves auditing and governance
- Supports least privilege

---

## 💼 Real Scenario

Instead of assigning roles to multiple users individually:
- Create a role group (e.g. Helpdesk_Admins)
- Assign role to the group
- Add users to the group

---

## 🏷️ Naming Convention (IMPORTANT)

### Format:
Company_Function_Role_Scope

### Examples:
- Contoso_Helpdesk_Admins
- Contoso_Security_Admins
- Contoso_Exchange_Admins
- Contoso_Global_Readers

### Best Practices:
- Keep names clear and consistent
- Use underscores (_) instead of spaces
- Include department or role
- Avoid overly long names

---

## ⚙️ Creating Role Groups

- Create Security or Microsoft 365 group
- Enable: "Assignable to role"
- Assign roles to the group
- Add users as members

👉 Can be done via:
- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- PowerShell / Microsoft Graph (scripts available)

---

## 🔒 Security & Restrictions

- Only Global Admin or Privileged Role Admin can create
- Membership type must be Assigned (no dynamic groups)
- Cannot convert existing group into role group
- Max 500 role groups per tenant
- No group nesting allowed
- Special permissions required for management

---

## 🚨 Security Risk & Protection

Risk:
- Admin adds themselves to role group → privilege escalation

Protection:
- Restricted membership control
- Only authorised admins can manage role groups

---

## ⏱️ Role Groups + PIM

- Use Privileged Identity Management (PIM)
- Make roles temporary (just-in-time access)
- Reduces security risk

---

## 📜 Licensing

- Entra ID P1 → required for role groups
- Entra ID P2 → required for PIM

---

## 🤝 Delegated Administration (Partners)

### What It Is:
- Outsourcing Microsoft 365 admin tasks to a partner

---

### How It Works:
- Partner sends request email
- Organisation approves access

---

### Steps to Approve:
- Open email
- Review terms
- Click approval link
- Select "Yes" for delegated admin

---

### Roles Partners Can Have

#### Full Administration:
- Full access (similar to Global Admin)
- Manage users, licences, domains, security
- Access data and services

#### Limited Administration:
- Restricted access
- Manage users and passwords
- View service health
- Handle support tickets
- Cannot manage security or domains

---

## ⚠️ Security Considerations

- Partners may access sensitive data
- Only grant necessary permissions
- Clearly define responsibilities
- Regularly review access

---

## ✅ Best Practices

- Use role groups instead of direct role assignment
- Apply least privilege
- Use clear naming conventions
- Audit roles regularly
- Use PIM for temporary access
- Document role assignments
- Limit Global Admins
- Review delegated partner access

---

## 🎯 Interview Questions

Q1: What is a role group?  
A group with roles assigned to it

Q2: Why use role groups?  
To simplify and standardise access management

Q3: Can role groups be dynamic?  
No, only assigned membership

Q4: Who can create role groups?  
Global Admin or Privileged Role Admin

Q5: What is delegated administration?  
Giving a partner admin access to manage your tenant

Q6: What are partner roles?  
Full Admin and Limited Admin

---

## 🧠 Summary

- Role groups simplify permission management
- Assign roles to groups, not users
- Use naming standards for clarity
- Combine with PIM for security
- Be cautious when delegating admin access to partners

---
