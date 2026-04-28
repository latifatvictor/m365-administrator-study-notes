# Dynamic Groups – Microsoft Entra (Quick Notes)

---

## 🔑 Key Points

- Dynamic groups = automatic membership based on rules
- Works for:
  - Security Groups
  - Microsoft 365 Groups
- No manual add/remove users
- Updates automatically when user/device attributes change

---

## ⚠️ Requirements

- Microsoft Entra ID P1 license (or higher)
- Must cover all users in dynamic groups

---

## 🧠 Rule Basics

Format:
Property Operator Value

Example:
user.department -eq "Sales"

---

## 🔧 Common Rules

All users:
user.objectId -ne null

Department:
user.department -eq "HR"

Multiple departments:
user.department -in ["HR","Finance"]

Exclude guests:
(user.objectId -ne null) -and (user.userType -eq "Member")

---

## ⚠️ Important Limitations

- Cannot manually manage members
- Cannot mix users + devices
- Device rules ≠ user attributes
- Rule builder = max 5 expressions

---

## 💼 Real Work Scenarios

- Auto-add new employees to department groups
- Assign licenses using group-based licensing
- Apply Conditional Access by department
- Automatically remove access when user changes role

---

## 🎯 Why It Matters (In Real Jobs)

- Saves time (no manual user management)
- Reduces errors
- Keeps access always up-to-date
- Essential in large organisations

---

## 🔥 Interview Questions

Q1: What is a dynamic group?
A: A group where membership is automatically assigned using rules

Q2: Can you manually add users?
A: No

Q3: What license is required?
A: Microsoft Entra ID P1 or higher

Q4: What happens when user attributes change?
A: Group membership updates automatically

Q5: When would you use dynamic groups?
A: When you want automated access control based on attributes like department or role

---

## 🧠 Summary

- Dynamic groups = automation + scalability
- Rule-based membership
- Critical for modern cloud environments
