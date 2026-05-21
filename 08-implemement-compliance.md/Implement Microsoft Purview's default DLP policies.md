## Implement Microsoft Purview Default DLP Policies – Summary

### Overview:
Before creating custom policies, Microsoft Purview provides **two default DLP policies** to help organizations immediately start protecting sensitive data:

- ✅ Default policy for devices  
- ✅ Default policy for Teams  

These policies offer **out-of-the-box protection** with minimal configuration.

---

## 1. Default Policy for Devices

### Purpose:
- Detect and notify when users **share sensitive information externally**

---

### What It Monitors:
- Exchange Online (email)
- SharePoint Online
- OneDrive  

---

### Sensitive Data Detected:
- Credit card numbers  
- Source code (via classifier)  
- Healthcare data (HIPAA template)  
- Intellectual property (e.g., M&A, product development, security docs)  

---

### Default Behavior:
- ✅ Detects external sharing  
- ⚠️ Shows **policy tips** to users  
- 📧 Sends **email notifications**  
- 📊 Generates activity reports  

---

### What You Can Do:
- View reports (last 30 days activity)  
- See:
  - Who shared sensitive data  
  - When and how it was shared  
- Refine the policy easily  

---

### Customization Options:
- Send incident reports to admins  
- Add multiple recipients for alerts  
- Block sharing (with or without override)  
- Modify detection rules  

---

### Key Notes:
- Appears as a tile in Purview portal  
- Policy matches may take up to **48 hours** to appear  
- Fully customizable or can be disabled/deleted  

---

## 2. Default Policy for Teams

### Purpose:
- Monitor sensitive data shared in:
  - Teams chats  
  - Channel messages  

---

### Default Behavior:
- ✅ Tracks sensitive data sharing (internal & external)  
- ⚠️ Does NOT show policy tips to users  
- 📧 Sends **low-severity alerts to admins**  
- ✅ Generates alert events  

---

### Key Features:
- Enabled by default for all users  
- Admin must configure:
  - Alert recipients  

---

### What Admins Can Do:
- View activity in compliance portal  
- Edit or delete the policy  
- Customize rules and alerts  

---

## Viewing & Refining Policies:

### Access:
- Microsoft Purview Compliance Portal → **DLP Policies**

---

### Reports Include:
- Number of sensitive items shared  
- Data categories involved  
- User activity (who, what, when)  

---

### Refinement Options:
- Adjust sensitivity thresholds  
- Add alerting rules  
- Enable blocking actions  
- Configure override options  

---

## Further Protect Shared Content Widget

### When It Appears:
- No existing DLP policies  
- Sensitive data shared externally in last 30 days  

---

### Function:
- Provides quick setup guidance  
