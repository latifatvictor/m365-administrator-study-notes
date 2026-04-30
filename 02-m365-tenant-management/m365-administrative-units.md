# Microsoft Entra Administrative Units (MS-102)

---

## 📌 What are Administrative Units?

- Containers in Microsoft Entra ID
- Hold:
  - Users
  - Groups
  - Devices
- Used to **scope admin permissions**

---

## 🎯 Purpose

- Restrict admin access to a specific part of the organisation
- Enable delegated administration (by region, department, etc.)

---

## 💼 Real Work Scenario

University example:
- Create AU: "School of Business"
- Add students & staff
- Assign IT admins to manage ONLY that school

---

## 🧠 Key Concept

- Admin roles can be **scoped to an Administrative Unit**
- Admin manages ONLY resources inside that unit

---

## 📍 Examples of Use

- Geography → London, New York
- Department → HR, Marketing
- Business Units → Finance, Sales

---

## 🔁 Membership

- A user can belong to **multiple administrative units**
- Example:
  - London + Marketing

---

## ⚙️ What You Can Do

- Create administrative units
- Add/remove users, groups, devices
- Assign scoped admin roles
- Use dynamic membership (rules)

👉 Can be managed via:
- Microsoft Entra Admin Center
- PowerShell / Microsoft Graph (scripts available)

---

## 🔐 Permissions Scope

✔ Admin CAN:
- Manage users in their AU
- Reset passwords
- Manage devices/groups in scope

❌ Admin CANNOT:
- Manage users outside their AU

⚠️ Important:
- AUs only restrict **admin actions**
- Users can still view other users in some tools

---

## ⚠️ Important Behaviour

- Adding a group to AU ≠ managing its members
- Must add users individually to manage them

---

## 🚫 Limitations

- No nesting of administrative units
- Scoped admins cannot create/delete users
- Roles cannot be globally applied across all AUs
- AU scope does NOT apply automatically to group members
- Limited integration with some services

---

## 🔄 Lifecycle of Administrative Units

1. Creation (based on structure)
2. Growth (more units added)
3. Cleanup (remove unused)
4. Stabilisation

---

## 📜 Licensing

- Entra ID P1 → required for admins
- Entra Free → for members
- P1 required for dynamic membership

---

## 🔒 Security Best Practices

- Use AUs for delegation instead of Global Admin
- Align AUs with organisational structure
- Regularly review membership
- Avoid over-complication
- Combine with least privilege

---

## 🎯 Interview Questions

Q1: What is an Administrative Unit?  
A container used to scope admin permissions

---

Q2: Why use Administrative Units?  
To restrict admin access to specific users/groups

---

Q3: Can a user belong to multiple AUs?  
Yes

---

Q4: Do AUs restrict user visibility?  
No, only admin permissions

---

Q5: Can you nest AUs?  
No

---

Q6: What is a key limitation?  
Group members are not automatically scoped

---

## 🧠 Summary

- Administrative Units = scoped admin control
- Used for delegation (region, department)
- Improve security and organisation
- Work alongside RBAC model
- Must be carefully planned

---
