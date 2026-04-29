# DNS Zone Planning (Microsoft 365) 
---

## 🔑 Key Idea

- Public DNS is REQUIRED for Microsoft 365 to work
- Without it → email, Teams, SharePoint will fail

---

## 🌐 Why Public DNS Matters

- ✔ Domain verification → TXT record
- ✔ Email delivery → MX record
- ✔ Outlook setup → Autodiscover
- ✔ SSO / Federation → DNS records
- ✔ Apps & services → CNAME / A records

---

## 🧠 Hybrid DNS (Most Real-World Scenario)

### 1. Split DNS (VERY IMPORTANT)

Same domain, different results:

- Internal → private IP (192.168.x.x)
- External → public IP

✔ Example:
mail.contoso.com  
- Internal → 192.168.1.10  
- External → Microsoft 365 endpoint  

👉 This is the **correct answer in exams/interviews**

---

### 2. DNS Forwarding

- Internal DNS → forwards unknown queries to internet DNS
- Ensures Microsoft 365 services resolve

---

### 3. Namespace Design

- Single → contoso.com  
- Split → internal.contoso.com + cloud.contoso.com  

---

### 4. DNS Sync

- Internal + external DNS must match for M365 records
- Prevents login/email issues

---

## 🏗️ DNS Design Options

### Option 1: Different Names

- Internal → contoso.local  
- External → contoso.com  

✔ Simple  
❌ Less modern

---

### Option 2: Split DNS (Recommended)

- Same domain everywhere
- Different IP responses

✔ Most used in real jobs  
✔ Best for hybrid/cloud

---

## ☁️ Cloud-Only DNS

- Use providers:
  - Azure DNS
  - GoDaddy
  - Cloudflare

Focus:
- Correct DNS records
- High availability
- No on-prem dependency

---

## 🔐 Security

- Use DNSSEC
- Restrict DNS access
- Monitor DNS changes

---

## 💼 Real Work Scenarios

- Outlook not connecting → Autodiscover issue
- Emails bouncing → MX misconfigured
- Teams login failing → DNS resolution problem
- Migration → DNS cutover planning
- Hybrid → split DNS not configured properly

---

## ⚠️ Common Mistakes

- No public DNS ❌
- Wrong MX record ❌
- Missing Autodiscover ❌
- DNS not synced ❌

---

## 🎯 Why It Matters

- DNS issues = #1 cause of M365 outages
- Affects:
  - Email
  - Login
  - App access

---

## 🔥 Interview Questions

Q1: Why is public DNS required?  
A: For verification, email routing, and service discovery  

---

Q2: What is split DNS?  
A: Same domain resolves differently internally vs externally  

---

Q3: What is DNS forwarding?  
A: Internal DNS forwards unknown queries to external DNS  

---

Q4: What happens if MX is wrong?  
A: Emails won’t be delivered  

---

Q5: Most common DNS setup in hybrid?  
A: Split DNS  

---

Q6: Exam Question (VERY IMPORTANT)

Scenario:  
Internal + external DNS use SAME domain  

Answer:  
👉 Configure **Split Brain DNS (Split DNS)**  

---

## 🧠 Summary

- Public DNS = mandatory
- Split DNS = most practical solution
- DNS misconfig = major real-world issue
