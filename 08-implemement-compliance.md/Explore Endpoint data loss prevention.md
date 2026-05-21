## Endpoint Data Loss Prevention (Endpoint DLP) – Microsoft Purview Summary

### Overview:
- **Endpoint DLP** extends Microsoft Purview DLP to **user devices**
- Protects sensitive data stored on:
  - ✅ Windows 10 / Windows 11  
  - ✅ macOS (latest 3 versions)

👉 Enables organizations to:
- Monitor user activity on devices  
- Detect risky behavior  
- Prevent data exfiltration  

---

## Key Capabilities:

### 1. Monitor Sensitive Data on Devices
- Tracks user interactions with sensitive files:
  - Data at rest (stored locally)
  - Data in use (being edited/copied)
  - Data in motion (being shared/transferred)

✅ Integrated with:
- Activity Explorer  
- DLP policies  

---

### 2. Real-Time Policy Enforcement
- Policies are evaluated **centrally**
- Updates sync within ~1 hour  

✅ No need to deploy policies manually to each device  

---

### 3. Visibility & Insights
- Shows:
  - Who accessed data  
  - What action was taken  
  - Where data was moved  

---

## Supported Endpoint Activities:

### Key Activities Monitored & Controlled:

| Activity | Description | Control |
|---------|------------|--------|
| Upload to cloud | Upload to unapproved apps | ✅ Audit & Block |
| Copy to apps | Paste sensitive data to another app | ✅ Audit & Block |
| Copy to USB | Transfer to removable storage | ✅ Audit & Block |
| Copy to network share | Move data to shared drives | ✅ Audit & Block |
| Print | Print sensitive documents | ✅ Audit & Block |
| Remote desktop copy | Transfer via remote session | ✅ Audit & Block |
| Bluetooth transfer | Send via Bluetooth apps | ✅ Audit & Block |
| File creation/rename | Track file changes | ✅ Audit only |

---

## Example Use Case:
- Goal:
  - Prevent Finance team from leaking credit card data  

### Steps:
1. Create DLP policy  
2. Scope to:
   - Endpoint devices  
   - Finance users  
3. Define condition:
   - Sensitive info type = Credit Card Number  
4. Configure action:
   - 🚫 Block all risky actions  

---

## File Monitoring:

### Supported File Types:
- Word, Excel, PowerPoint  
- PDF, CSV, TXT  
- Code files (.cs, .java, etc.)  

---

### File Type Categories:
- Word processing (DOC, PDF)
- Spreadsheets (XLS, CSV)
- Presentations (PPT)
- Archives (ZIP, RAR)
- Email files (PST, MSG)

---

### Important Note:
- Can monitor:
  - All files  
  - OR only files matched by policy  

---

## Always Audit Option:
- When enabled:
  - ✅ Logs all activity (even without policy match)  

- When disabled:
  - ✅ Only logs policy-related events  

---

## Device Onboarding:

### Required Step:
- Devices must be **onboarded** before monitoring  

---

### Methods:
- Microsoft Intune  
- Group Policy  
- Microsoft Endpoint Configuration Manager  
- Local scripts  
- VDI scripts  

---

✅ Devices onboarded via Defender for Endpoint:
- Automatically appear in device inventory  

---

## Device Management:
- Collects data from:
  - User activities  
  - File interactions  
- Feeds into:
  - Endpoint DLP  
  - Insider Risk Management  

---

## Viewing Endpoint DLP Data:

### 1. Activity Explorer
- Displays:
  - Timeline of user activity  
  - Sensitive file interactions  
- Includes:
  - File name  
  - User  
  - Device  
  - Action performed  

---

### 2. Alerts Dashboard
- Shows:
  - Policy violations  
  - Triggered alerts  
- Enables:
  - Triage and investigation  

---

## Example Logged Data:
- File name and size  
- User identity  
- Device name  
- Action (copy, print, upload)  
- Location (source/destination)  
- Application used  
- USB device details (if applicable)  

---

## Requirements:

### Licensing:
- Microsoft 365 E5 / A5  
- Compliance or Information Protection add-ons  

---

### Connectivity:
- Devices must communicate with:
  - Microsoft cloud DLP service  

---

## Best Practices:
- ✅ Start with monitoring (audit mode)  
- ✅ Focus on high-risk activities (USB, cloud upload)  
- ✅ Use endpoint policies with user-based scoping  
- ✅ Combine with Insider Risk Management  
- ✅ Tune policies to reduce false positives  

---

## Key Takeaway:
Endpoint DLP extends protection beyond cloud services to **user devices**, enabling organizations to:
- Monitor sensitive data usage  
- Prevent data leaks at the source  
- Enforce security policies in real time  

➡️ It provides **comprehensive endpoint-level data protection**, ensuring sensitive information is safeguarded wherever users interact with it
