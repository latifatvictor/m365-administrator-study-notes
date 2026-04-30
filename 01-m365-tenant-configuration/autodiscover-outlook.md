# Outlook Autodiscover (Automatic Client Configuration)

---

## 🔑 Key Concept

Autodiscover automatically configures Outlook profiles  
➡ No manual server settings needed

---

## ⚙️ How It Works (Step-by-Step)

1. User opens Outlook  
2. Enters email + password  
3. Outlook checks DNS for Autodiscover record  
4. Finds Microsoft 365 Autodiscover service  
5. Authenticates user  
6. Receives config (XML format)  
7. Outlook auto-configures mailbox  
8. Connects to Exchange Online  

---

## 🌐 Key DNS Record

CNAME:
autodiscover → autodiscover.outlook.com

---

## 💼 Real Work Scenarios

- User sets up Outlook → works instantly (Autodiscover working)  
- Outlook keeps asking for password → Autodiscover issue  
- Mail profile fails → missing/incorrect DNS record  
- Hybrid setup → Outlook may connect to on-prem first  

---

## ⚠️ Common Issues

- Missing Autodiscover record  
- Wrong DNS pointing to old Exchange  
- Firewall blocking access  
- Credential mismatch  

---

## 🔧 Troubleshooting Tips

- Run Outlook test (Ctrl + Right-click Outlook icon → Test E-mail AutoConfiguration)  
- Check DNS:
  nslookup autodiscover.domain.com  
- Confirm CNAME is correct  

---

## 🎯 Interview Questions

Q1: What is Autodiscover?  
A: A service that automatically configures Outlook profiles  

---

Q2: What DNS record is required for Autodiscover?  
A: CNAME → autodiscover.outlook.com  

---

Q3: What happens if Autodiscover fails?  
A: Outlook cannot configure mailbox automatically  

---

Q4: How do you troubleshoot Autodiscover?  
A: Check DNS, run Outlook test tool, verify credentials  

---

Q5: What format does Autodiscover return settings in?  
A: XML  

---

## 🧠 Summary

- Autodiscover = automatic Outlook setup  
- Relies on DNS (CNAME record)  
- Critical for user experience  
- Most issues = DNS misconfiguration
