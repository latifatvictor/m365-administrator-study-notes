# DNS Zone Planning for Microsoft 365 (Quick Notes)

---

## 🔑 Key Concept

- DNS = backbone of Microsoft 365 services
- Required for:
  - Email (Exchange Online)
  - Teams
  - SharePoint
  - Authentication (SSO)

---

## 🌐 Why Public DNS is Required

- Domain verification → TXT record
- Email delivery → MX record
- Autodiscover → Outlook config
- Federation → SSO & hybrid
- Web apps → CNAME / A records

---

## 🧠 Core DNS Records

- A → maps domain to IP
- CNAME → alias (e.g. autodiscover)
- MX → mail routing
- TXT → verification/security
- SRV → service discovery

---

## 🔄 Hybrid DNS Planning (REAL IMPORTANT)

### 1. Namespace Design

- Single namespace → contoso.com
- Split namespace → 
  - internal.contoso.com
  - cloud.contoso.com

---

### 2. DNS Forwarding

- Internal DNS → forwards to public DNS
- Ensures external services resolve correctly

---

### 3. Split DNS (VERY COMMON)

Same domain, different results:

- Internal user → private IP (192.168.x.x)
- External user → public IP

✔ Example:
mail.contoso.com  
- Internal → 192.168.1.10  
- External → 52.96.x.x  

---

### 4. DNS Synchronisation

- Keep internal + external DNS aligned
- Prevents login / service failures

---

### 5. Service Discovery

- Uses:
  - SRV records
  - Autodiscover
- Helps apps find services automatically

---

## ☁️ Cloud-Only DNS Planning

- No on-prem dependency
- Use providers like:
  - Azure DNS
  - GoDaddy
  - Cloudflare

### Key Focus:
- Clean DNS structure
- Proper record configuration
- High availability

---

## 🏗️ DNS Zone Design Options

### Option 1: Different Internal & External Domains

- Internal → contoso.local  
- External → contoso.com  

✔ Simple  
❌ Not modern best practice

---

### Option 2: Split DNS (Recommended)

- Same domain internally + externally
- Different IP responses

✔ Most common in real-world  
✔ Supports hybrid + cloud

---

## 🔐 Security Considerations

- DNSSEC (protect DNS integrity)
- Firewalls
- Access control to DNS changes

---

## 💼 Real Work Scenarios

- Outlook not connecting → Autodiscover DNS issue
- Emails not received → wrong MX record
- Teams login issue → DNS resolution failure
- Hybrid setup → split DNS misconfigured
- Migration → DNS cutover planning

---

## ⚠️ Common Mistakes

- No public DNS → services won’t work ❌
- Wrong MX → email failure ❌
- Missing autodiscover → Outlook issues ❌
- Not syncing DNS zones → login failures ❌

---

## 🎯 Why It Matters

- Directly impacts:
  - Email delivery
  - User login
  - App connectivity
- One of the MOST common real IT issues

---

## 🔥 Interview Questions

Q1: Why is public DNS required for Microsoft 365?  
A: For domain verification, email routing, and service discovery

---

Q2: What is split DNS?  
A: Same domain resolves differently internally vs externally

---

Q3: What happens if MX records are incorrect?  
A: Emails won’t be delivered

---

Q4: What is Autodiscover used for?  
A: Automatically configures Outlook/email clients

---

Q5: What is DNS forwarding?  
A: Internal DNS forwards unknown queries to external DNS

---

Q6: What DNS setup is most common in hybrid environments?  
A: Split DNS

---

## 🧠 Summary

- DNS is critical for Microsoft 365 functionality
- Public DNS is mandatory
- Split DNS = most practical setup
- Misconfigured DNS = major real-world issue
