# Microsoft 365 Admin Role Best Practices

---

## 🔑 Core Idea

👉 Security = RIGHT access + RIGHT time + RIGHT scope  

---

## 🔐 1. Least Privilege (MOST IMPORTANT)

- Give only the access needed
- Avoid “just in case” permissions

✔ Think:
- What do they need?
- Where do they need it?
- How long do they need it?

---

### 💼 Real Scenario
Helpdesk needs password reset →  
❌ Don’t give Global Admin  
✅ Give Helpdesk Admin

---

## ⏱️ 2. Use PIM (Just-In-Time Access)

- No permanent high-level access
- Admin activates role only when needed

✔ Benefits:
- Reduces risk
- Automatic removal after time

---

### 💼 Real Scenario
Security admin activates role for 1 hour to investigate incident

---

## 🔐 3. Enforce MFA for ALL Admins

- Protects against compromised passwords
- Reduces risk by 99.9%

✔ Use:
- Conditional Access OR
- PIM role settings

---

### 💼 Real Scenario
Attacker gets password →  
MFA stops access

---

## 🔄 4. Use Access Reviews

- Regularly check who still needs access
- Remove unused permissions

✔ Why?
- People change roles
- Accounts get forgotten

---

### 💼 Real Scenario
Old IT staff still has admin access → removed during review

---

## 👑 5. Limit Global Administrators

- Keep between **2–4 admins**
- Never more than 5

✔ Why?
- Full access = highest risk

✔ Always:
- Protect with MFA

---

### 🚨 Bonus: Break Glass Accounts
- 2 emergency Global Admin accounts
- No normal MFA dependency
- Used only in emergencies

---

## 👥 6. Use Groups for Role Assignment

- Assign roles to groups, not individuals
- Easier to manage

✔ Benefit:
- Add/remove user → role updates automatically

---

### 💼 Real Scenario
IT Admin group → has Exchange + Teams roles  
New admin joins → just add to group

---

## ☁️ 7. Use Cloud-Only Admin Accounts

- Avoid synced on-prem accounts for admin roles

✔ Why?
- If on-prem is compromised → cloud is also at risk

---

## ⚠️ Common Mistakes

- Too many Global Admins  
- No MFA on admin accounts  
- Permanent high-level access  
- Assigning roles directly instead of groups  
- Not reviewing access regularly  

---

## 🔥 Interview Questions

### Q1: What is least privilege?
Giving users only the permissions they need to perform their job.

---

### Q2: What is PIM?
Privileged Identity Management allows temporary (just-in-time) admin access.

---

### Q3: Why limit Global Administrators?
They have full control, so fewer accounts reduce attack surface.

---

### Q4: Why use MFA for admins?
To prevent unauthorized access even if passwords are compromised.

---

### Q5: What are access reviews?
Regular checks to ensure only the right users have access.

---

### Q6: Why use groups for role assignment?
Easier management and scalability.

---

### Q7: What is a break glass account?
Emergency admin account used when normal access fails.

---

## 🧠 Summary

- Always follow least privilege  
- Use PIM for temporary access  
- Enforce MFA everywhere  
- Review access regularly  
- Limit Global Admins  
- Use groups instead of individuals  
- Prefer cloud-only admin accounts  
