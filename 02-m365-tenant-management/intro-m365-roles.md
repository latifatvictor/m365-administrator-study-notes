# Microsoft 365 Roles & Permissions (Introduction)

---

## 🔑 Key Concept

Microsoft 365 uses **admin roles** to control:
➡ Who can do what in the environment

✔ Based on **least privilege principle**
✔ Avoid giving full admin access unnecessarily

---

## 🧠 What You Need to Know

- Roles = permissions assigned to users  
- Each role = specific tasks (e.g. user management, billing)  
- Managed via:
  - Microsoft 365 admin center  
  - Microsoft Entra ID  

---

## 👤 Common Admin Roles

- Global Administrator → full access  
- User Administrator → manage users/licenses  
- Billing Administrator → manage subscriptions  
- Service Admin → manage specific services (Exchange, Teams)  

---

## 👥 Role Groups (IMPORTANT)

✔ Instead of assigning roles to users directly:

- Create a group  
- Assign roles to the group  
- Add users to the group  

👉 Users inherit permissions automatically  

---

## 🔐 Advanced Permission Control

### 1. Administrative Units
- Scope admin permissions to specific users/groups  
- Example: Admin only manages London users  

---

### 2. Privileged Identity Management (PIM)

✔ Just-in-time access  
✔ Temporary admin roles  
✔ Reduces security risk  

---

## 🤝 Delegating to Partners

- External partners can be given limited admin roles  
- Must monitor and revoke access when needed  

---

## 💼 Real Work Scenarios

- Helpdesk staff → User Administrator role  
- Finance team → Billing Administrator  
- Avoid giving Global Admin to everyone  
- Use PIM for temporary admin tasks  

---

## ⚠️ Common Mistakes

- Too many Global Admins  
- No role separation  
- No monitoring of admin activity  
- Permanent high-level access  

---

## 🎯 Interview Questions

Q1: What is the purpose of roles in Microsoft 365?  
A: To control access and permissions  

---

Q2: What is the most powerful role?  
A: Global Administrator  

---

Q3: Why use role groups?  
A: Easier management and consistent permissions  

---

Q4: What is PIM?  
A: Provides temporary, just-in-time admin access  

---

Q5: What is the principle of least privilege?  
A: Give only the minimum access required  

---

## 🧠 Summary

- Roles control access  
- Use least privilege  
- Prefer groups over direct assignment  
- Use PIM for security  
