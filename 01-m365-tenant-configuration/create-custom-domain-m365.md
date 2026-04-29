# Create a Custom Domain in Microsoft 365 (Quick Notes)

---

## 🔑 Key Concept

A custom domain (e.g. contoso.com) allows users to:
- Use professional email (user@contoso.com)
- Connect services like Exchange, Teams, SharePoint

---

## 🧠 Step-by-Step Process

### 1. Verify Domain Ownership

✔ Method (MOST COMMON):
- Add TXT record in DNS

Example:
Host: @  
Value: MS=xxxxxxxx  

✔ Alternative:
- Use MX record (temporary)

---

### 2. Add Domain in Microsoft 365

Path:
Settings → Domains → Add domain

---

### 3. Configure DNS Records

#### Required for Email (Exchange Online)

- MX → mail routing  
- CNAME (Autodiscover) → Outlook setup  
- TXT (SPF) → anti-spoofing  

✔ Example SPF:
v=spf1 include:spf.protection.outlook.com -all

---

#### Required for Teams

- SRV → federation  
- CNAME → lyncdiscover  

---

### 4. Verify DNS Propagation

- Takes minutes to hours
- Use tools like:
  - nslookup
  - online DNS checkers

---

## 💼 Real Work Scenarios

- New company setup → add custom domain for branding  
- Email migration → update MX to Microsoft 365  
- Users not receiving emails → MX misconfigured  
- Outlook not connecting → Autodiscover missing  

---

## ⚠️ Common Issues

- Domain verified but services not working → missing DNS records  
- Emails still going to old system → MX not updated  
- Multiple SPF records → email delivery failure  
- DNS propagation delay → changes not immediate  

---

## 🔥 Important Tips

- Add domain BEFORE creating users (saves time)  
- Remove old MX records after migration  
- Only ONE SPF record allowed  
- Always validate DNS after changes  

---

## 🎯 Interview Questions

Q1: How do you verify a domain in Microsoft 365?  
A: Add a TXT record to DNS and verify in admin centre  

---

Q2: What is the role of MX record?  
A: Routes incoming email to Microsoft 365  

---

Q3: What happens if MX is not updated?  
A: Emails continue going to old mail system  

---

Q4: What is DNS propagation?  
A: Time it takes for DNS changes to update globally  

---

Q5: Why is SPF important?  
A: Prevents email spoofing and improves deliverability  

---

Q6: What is Autodiscover used for?  
A: Automatically configures Outlook profiles  

---

## 🧠 Summary

- Verify domain → Add DNS → Connect services  
- MX, SPF, Autodiscover = critical  
- Most real issues = DNS misconfiguration
