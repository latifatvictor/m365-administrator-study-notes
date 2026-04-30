# Microsoft 365 Permission Model (Roles, Scopes, Assignments)

---

## 🔑 Key Concept

Microsoft 365 permissions are built on 3 things:

➡ Roles → What you can do  
➡ Scopes → Where you can do it  
➡ Assignments → Who gets access  

---

## 🧠 1. Roles (WHAT you can do)

Roles = collection of permissions

### Types:
- Built-in roles → Default (e.g. Global Admin, Exchange Admin)
- Custom roles → Created for specific needs

✔ Example:
User Administrator → can manage users but NOT everything

---

## 🌍 2. Scopes (WHERE you can do it)

Scopes limit access

### Types:

✔ Directory Scopes  
- Based on users/org structure  
- Example: Only manage London users  

✔ Management Scopes  
- Based on service  
- Example: Only manage Exchange mailboxes  

---

## 🔗 3. Assignments (WHO gets access)

Links roles + scopes to users

### Types:

✔ Direct Assignment  
- Assign role directly to user  
- Simple but less scalable  

✔ Indirect Assignment  
- Through groups or rules  
- Dynamic and automated  

---

## 🧩 Types of Roles

### 1. Global Roles
- Full access across Microsoft 365  
- Example: Global Administrator  

---

### 2. Service Roles
- Specific service access  
- Example:
  - Exchange Admin  
  - Teams Admin  
  - SharePoint Admin  

---

### 3. Feature Roles
- Specific function access  
- Example:
  - Security Admin  
  - Compliance Admin  
  - Intune Admin  

---

## 📊 Role Categories

- Administrator → Full control  
- Reader → View only  
- Application → App access (Power BI, Power Apps)  

---

## 💼 Real Work Scenarios

- Helpdesk → User Administrator  
- Security team → Security Admin  
- Auditor → Global Reader  
- Department IT → Scoped admin (only their department)  

---

## ⚠️ Common Mistakes

- Too many Global Admins  
- No role scoping  
- Assigning roles directly instead of using groups  
- No control over admin access  

---

## 🔐 Best Practices

- Use least privilege  
- Use groups instead of direct assignment  
- Apply scopes (limit access)  
- Use PIM for temporary access  

---

## 🎯 Interview Questions

Q1: What are the 3 components of M365 permission model?  
A: Roles, Scopes, Assignments  

---

Q2: Difference between role and scope?  
A: Role = what you can do, Scope = where you can do it  

---

Q3: What is direct vs indirect assignment?  
A: Direct = assign to user, Indirect = via group/rule  

---

Q4: When would you use custom roles?  
A: When built-in roles are too broad  

---

Q5: Why are scopes important?  
A: To limit access and improve security  

---

## 🧠 Summary

- Roles = permissions  
- Scopes = limits  
- Assignments = who gets access  
- Combine all 3 for secure access control
