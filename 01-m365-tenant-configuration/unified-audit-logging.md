# Unified Audit Logging in Microsoft 365

---

## 🔑 Key Concepts (Must Know)

### What is Unified Audit Logging?

Unified Audit Logging records:

- user activities  
- admin activities  
- system events  

Across Microsoft 365 services:

- Exchange Online  
- SharePoint Online  
- OneDrive  
- Microsoft Teams  
- Power BI  
- Microsoft Entra ID  

👉 Key idea:
**Single, central log for all activity across Microsoft 365**

---

## 🧠 Why It Matters

Used for:

- security investigations  
- compliance tracking  
- troubleshooting issues  
- monitoring user activity  

👉 Real-world:
"Who deleted this file?"  
"Who accessed sensitive data?"  
Audit log answers these questions.

---

## 📊 What Gets Logged

### Examples of activities

- file access (download, upload, delete)  
- user sign-ins  
- admin changes  
- sharing activity  
- app configuration changes  

---

### Advanced logs include

- application administration  
- service principal changes  
- authentication changes  
- Defender activities  

---

## 📍 Where to Access Audit Logs

👉 Microsoft Purview Portal

Path:
Microsoft Purview → Audit → Search

---

## 🧠 Default Behaviour

- Audit logging is **ON by default**
- Logs retained for:
  - **180 days (standard)**

---

## ⏳ Retention Rules

- Logs before Oct 2023 → 90 days  
- Logs after Oct 2023 → 180 days  

👉 Can be extended up to **10 years** (with proper licensing)

---

## ⚠️ IMPORTANT WARNING

If auditing is turned OFF:

- No logs are recorded  
- No search results available  
- No data for:
  - Microsoft Sentinel  
  - Activity APIs  

👉 Real-world:
You lose visibility into security incidents

---

## ⚙️ How to Verify Audit Logging

### PowerShell (IMPORTANT)

```powershell
Get-AdminAuditLogConfig | Format-List UnifiedAuditLogIngestionEnabled
