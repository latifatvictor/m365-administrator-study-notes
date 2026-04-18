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

Result:
TRUE → enabled
FALSE → disabled
⚙️ How to Enable Audit Logging
Option 1: Microsoft Purview Portal
Go to Audit section
Click "Start recording user and admin activity"
Option 2: PowerShell
Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
⏱️ Important Note
May take up to 1 hour before logs become searchable
🔔 Additional Audit Features
1. Audit Retention Policies
Control how long logs are stored
Configurable per service/activity
2. Audit Search
Filter by:
date
user
activity
service
Export results to:
CSV
Azure storage
3. Audit Alerts
Trigger alerts based on events

👉 Example:

multiple failed login attempts
unusual file access
4. Reports
Prebuilt audit reports available
Useful for compliance and monitoring
💼 Real-Life IT Tasks
investigating suspicious login activity
checking who deleted or modified files
auditing admin actions
exporting logs for security teams
creating alerts for unusual behaviour
supporting compliance audits
⚠️ Common Mistakes
not verifying audit logging is enabled
ignoring retention policies
not setting up alerts
assuming logs are stored forever
turning off auditing accidentally
🔥 Interview Questions
Q1: What is Unified Audit Logging?

👉 Answer:
A centralized logging system in Microsoft 365 that records user and admin activities across services for security, compliance, and monitoring.

Q2: Where do you access audit logs?

👉 Answer:
In the Microsoft Purview portal under the Audit section.

Q3: How long are audit logs retained?

👉 Answer:
By default 180 days, but can be extended with retention policies.

Q4: What happens if audit logging is turned off?

👉 Answer:
No activities are recorded, and no audit data is available for investigation or monitoring.

Q5: How do you enable audit logging?

👉 Answer:
Through Microsoft Purview portal or using PowerShell with the Set-AdminAuditLogConfig cmdlet.

🧠 Summary
Unified Audit Log = central activity tracking system
Essential for:
security
compliance
investigations

👉 No audit logs = no visibility = high risk
