# DNS Records for Microsoft 365 (Quick Notes)

---

## 🔑 Key Concept

DNS records connect your domain to Microsoft 365 services like:
- Email (Exchange)
- Teams
- SharePoint
- Authentication

---

## 🧠 Core DNS Records (MUST KNOW)

### 1. TXT (Verification)
- Proves you own the domain
- Used during setup

✔ Example:
Host: @  
Value: MS=xxxxxxxx  

---

### 2. MX (Mail Flow)

- Routes emails to Microsoft 365

✔ Example:
contoso-com.mail.protection.outlook.com

❗ If wrong → emails NOT delivered

---

### 3. CNAME (Autodiscover)

- Helps Outlook auto-configure

✔ Example:
autodiscover → autodiscover.outlook.com

---

### 4. SPF (TXT Record)

- Prevents email spoofing

✔ Example:
v=spf1 include:spf.protection.outlook.com -all

❗ Only ONE SPF record allowed

---

## 📧 Email Required Records (Exchange Online)

- MX → mail delivery
- Autodiscover (CNAME) → Outlook setup
- SPF (TXT) → anti-spoofing

---

## 💬 Teams DNS Records

### SRV Records

- Enables Teams federation

✔ Example:
sipfederationtls → sipfed.online.lync.com

---

### CNAME

- lyncdiscover → webdir.online.lync.com

---

## 🔐 Security Records (IMPORTANT)

- SPF → basic protection
- DKIM → email signing
- DMARC → policy enforcement

👉 SPF alone is NOT enough

---

## 💼 Real Work Scenarios

- User can't receive emails → MX issue
- Outlook not setting up → Autodiscover missing
- Emails going to spam → SPF/DKIM problem
- Teams external chat not working → SRV record issue

---

## ⚠️ Common Mistakes

- Multiple SPF records ❌
- Wrong MX priority ❌
- Missing autodiscover ❌
- Not updating old mail server records ❌

---

## 🎯 Why It Matters

- Directly affects:
  - Email delivery
  - User login
  - Outlook setup
  - Teams connectivity

---

## 🔥 Interview Questions

Q1: What DNS records are required for Microsoft 365?
A: TXT, MX, CNAME, SRV

---

Q2: What does MX record do?
A: Routes incoming email to mail server

---

Q3: What is SPF?
A: TXT record that prevents email spoofing

---

Q4: Why is Autodiscover important?
A: Automatically configures Outlook

---

Q5: What happens if SPF is wrong?
A: Emails may go to spam or be rejected

---

Q6: Can you have multiple SPF records?
A: No, only ONE SPF record allowed

---

## 🧠 Summary

- DNS records = critical for M365
- MX, SPF, Autodiscover = most important
- Misconfiguration = real-world IT issues
