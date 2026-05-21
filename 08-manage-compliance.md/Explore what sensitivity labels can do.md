## What Sensitivity Labels Can Do – Microsoft Purview Summary

### Overview:
Once a sensitivity label is applied to a document or email, Microsoft 365 automatically **enforces all configured protection settings**. These labels go beyond classification—they actively **control access, usage, and security** of content.

---

# 🔐 1. Encrypt Content (Core Protection)

### What It Does:
- Protects data from unauthorized access  
- Controls:
  - Who can access content  
  - What actions they can perform  

---

### Examples:
- ✅ Internal users → Edit document  
- ✅ External partner → View only  
- ⏳ Set access expiry (time-limited access)  

---

### Flexibility:
- Admin-defined permissions  
- OR user-defined permissions (on label application)  

👉 Ensures **only authorized users** can open and use sensitive data  

---

# 🏷️ 2. Add Content Markings (Visual Protection)

### Types of Markings:
- 💧 Watermarks (documents only)  
- 🧾 Headers  
- 🧾 Footers  

---

### Purpose:
- Clearly indicate content sensitivity  
- Raise user awareness  

---

### Example:
- Header: *Confidential – Internal Use Only*  
- Watermark: *Highly Confidential*  

---

### Dynamic Markings:
- Can include variables like:
  - Label name  
  - Document name  

---

### Limits:
- Watermark: 255 characters  
- Headers/footers:
  - 1024 characters (except Excel: 255)  

---

# 🏢 3. Protect Containers (Sites, Teams, Groups)

### Applies To:
- Microsoft Teams  
- SharePoint sites  
- Microsoft 365 Groups  

---

### Controls Include:
- 🔒 Privacy settings (Public vs Private)  
- 🌍 External sharing restrictions  
- 🚫 Access from unmanaged devices  

---

### Key Point:
- Protects **location (container)**, not individual files  

---

# 🤖 4. Automatic or Recommended Labeling

### Automatic Labeling:
- Applied by system based on:
  - Content (e.g., sensitive data detected)  

---

### Recommended Labeling:
- Users receive suggestion:
  - Prompt appears  
- User decides:
  - ✅ Accept  
  - ❌ Reject  

---

### Benefit:
- Reduces manual effort  
- Improves classification accuracy  

---

# ⚙️ 5. How Protection Is Applied (By App)

| App | Content Markings | Encryption |
|-----|-----------------|-----------|
| Word / Excel / PowerPoint | Immediate | Immediate |
| Outlook (Desktop) | After send | Immediate |
| Outlook Web / Mobile | After send | After send |

---

# 🔄 6. Behavior Outside Office Apps

### When Labels Applied Outside Office:
- Examples:
  - Auto-labeling policies  
  - PowerShell  
  - Microsoft Defender for Cloud Apps  

---

### What Happens:
- ✅ Label metadata applied  
- ✅ Encryption applied  
- ❌ Content markings NOT applied immediately  

---

### When Opened in Office:
- Markings are applied:
  - On first save  

---

# 📊 7. Supported Scenarios Beyond Office

Sensitivity labels also work with:

---

### Power BI
- Label reports and datasets  
- Protect exported data  

---

### Azure / Purview
- Label:
  - SQL columns  
  - Storage assets  

---

### Third-Party Apps
- Through:
  - Microsoft Information Protection SDK  
- Enables external systems to:
  - Read labels  
  - Enforce protection  

---

# ✅ Example End-to-End Scenario:

### Situation:
- User creates financial report  

---

### Applied Label:
- “Highly Confidential”  

---

### System Automatically:
- 🔐 Encrypts file  
- 🚫 Prevents external sharing  
- 💧 Adds watermark  
- 👁️ Restricts access to authorized users  
- 🏢 Applies container-level restrictions (if applicable)  

---

# ⭐ Key Benefits:

- ✅ Strong data protection (encryption + access control)  
- ✅ Enhanced visibility (markings)  
- ✅ Automated classification (auto-labeling)  
- ✅ Consistent enforcement across platforms  
- ✅ Integration with multiple services  

---

# ⚠️ Important Notes:

- Labels behave differently depending on:
  - App used  
  - Where label is applied  
- Content markings may:
  - Appear later (depending on workflow)  

---

# ✅ Best Practices:

- ✅ Use encryption for sensitive labels  
- ✅ Add clear visual markings  
- ✅ Combine labels with auto-labeling  
- ✅ Use container labels for Teams/SharePoint  
- ✅ Test behavior across apps  
- ✅ Train users on label meaning  

---

# 🔑 Key Takeaway:
Sensitivity labels are more than just classification tags—they are **powerful enforcement tools** that:

- Control **who can access data**  
- Define **how data can be used**  
- Automatically apply **security controls across Microsoft 365**  

➡️ Enabling organizations to **protect, control, and govern sensitive data consistently and intelligently**
