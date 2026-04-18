# Complete Microsoft 365 Tenant Configuration

---

## 🔑 Key Concepts (Must Know)

### What is Tenant Completion?

Finalising tenant configuration means ensuring:

- all services are correctly set up  
- users can work without issues  
- security and compliance are enforced  

👉 Key idea:
This is the **go-live readiness checklist** for Microsoft 365

---

## 🧠 Why It Matters

- ensures smooth user onboarding  
- prevents security risks  
- avoids service disruptions  
- supports compliance requirements  

👉 Real-world:
A poorly configured tenant = user issues + security gaps

---

## ✅ Core Tenant Configuration Checklist

### 1. User & Mailbox Migration

- all users created  
- mailboxes working correctly  
- data successfully migrated  

👉 Real-world:
Users must be able to send/receive emails immediately

---

### 2. Permissions & Access

- correct roles assigned  
- least privilege applied  

👉 Example:
- Global Admin (limited users)
- Helpdesk roles for support staff  

---

### 3. Domain Configuration

- custom domain added (e.g. company.com)  
- domain verified  
- email addresses configured  

---

### 4. DNS & Mail Flow

- DNS records configured:
  - MX (mail flow)  
  - TXT (verification)  
  - CNAME (services)  

👉 Must test:
- email delivery  
- inbound/outbound flow  

---

### 5. Device Management (Intune)

- devices enrolled (Windows 10/11)  
- compliance policies applied  
- co-management configured (if hybrid)  

---

### 6. Mobile Device Governance

- mobile device policies  
- app protection policies  

👉 Real-world:
Protect company data on personal devices

---

### 7. Identity Synchronisation (if hybrid)

- Azure AD Connect configured  
- users synced from on-prem AD  

---

### 8. Multi-Factor Authentication (MFA)

- MFA enabled for users  
- especially admins  

👉 Critical for security

---

### 9. Security Enhancements

- Conditional Access policies  
- legacy authentication disabled  
- audit logging enabled  

---

### 10. Data Protection

- Data Loss Prevention (DLP) policies  
- Azure Information Protection (AIP)  

👉 Protect sensitive data

---

### 11. Monitoring & Reporting

- Microsoft Secure Score reviewed  
- improve security posture  

---

### 12. Ongoing Security Reviews

- regular policy reviews  
- update configurations  
- monitor risks  

---

## 🔍 Verifying Tenant Readiness

### Tools to Use

#### Microsoft Remote Connectivity Analyzer
- checks:
  - DNS configuration  
  - mail flow  

---

#### Microsoft Support and Recovery Assistant (SaRA)

- diagnoses:
  - connectivity issues  
  - Outlook problems  
  - Teams issues  

---

## 🧠 Advanced Concept: Tenant-to-Tenant Migration

### What is it?

- moving data between tenants  

### When used?

- mergers  
- acquisitions  
- restructuring  

👉 Important:
Complex and usually handled as a separate project

---

## 💼 Real-Life IT Tasks

- onboarding users after migration  
- verifying email flow  
- enrolling devices in Intune  
- enabling MFA for users  
- troubleshooting login issues  
- checking Secure Score  
- validating DNS records  

---

## ⚠️ Common Mistakes

- not verifying DNS records  
- forgetting to enable MFA  
- leaving legacy authentication enabled  
- incomplete mailbox migration  
- poor role assignment (too many admins)  

---

## 🔥 Interview Questions

### Q1: What should you check before going live with Microsoft 365?

👉 Answer:
User accounts, mailboxes, DNS configuration, security settings like MFA and Conditional Access, device management, and compliance configurations.

---

### Q2: Why is DNS configuration important?

👉 Answer:
It ensures proper mail flow, domain verification, and connectivity to Microsoft 365 services.

---

### Q3: What tools can you use to verify tenant setup?

👉 Answer:
Microsoft Remote Connectivity Analyzer and Microsoft Support and Recovery Assistant (SaRA).

---

### Q4: What is Secure Score?

👉 Answer:
A tool that helps measure and improve the security posture of a Microsoft 365 environment.

---

### Q5: Why should legacy authentication be disabled?

👉 Answer:
Because it doesn’t support modern security controls like MFA and is a major security risk.

---

## 🧠 Summary

- tenant configuration = full environment readiness  
- includes:
  - users  
  - security  
  - devices  
  - data protection  

👉 A well-configured tenant = secure + stable + productive environment
