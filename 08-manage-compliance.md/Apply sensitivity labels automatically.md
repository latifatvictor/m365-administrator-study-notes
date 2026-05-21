## Apply Sensitivity Labels Automatically – Microsoft Purview Summary

### Overview:
Automatic labeling allows Microsoft 365 to **apply sensitivity labels without user intervention** (or with minimal interaction). This helps organizations:
- ✅ Reduce user errors  
- ✅ Enforce consistent classification  
- ✅ Protect sensitive data at scale  

---

# 🔄 Two Methods of Auto-Labeling

---

## 1. Client-Side Auto-Labeling (User Interaction)

### Where It Happens:
- Inside Office apps:
  - Word, Excel, PowerPoint, Outlook  

---

### How It Works:
- Scans content while:
  - Editing documents  
  - Composing emails  
- Then:
  - ✅ Recommends a label (user decides)  
  - OR  
  - ✅ Automatically applies label (user can override)  

---

### Key Features:
- ⚡ Near real-time labeling  
- ✅ User sees and can approve/reject  
- ✅ Works before saving document  

---

### Limitations:
- Not supported in all Office versions  
- Requires compatible apps  

---

## 2. Service-Side Auto-Labeling (Policy-Based)

### Where It Happens:
- Microsoft 365 services:
  - SharePoint  
  - OneDrive  
  - Exchange (mail flow)  

---

### How It Works:
- Uses **autolabeling policies**
- Automatically applies labels:
  - ✅ To stored files (data at rest)  
  - ✅ To emails in transit  

---

### Key Features:
- ✅ Fully automated (no user interaction)  
- ✅ Works at scale across organization  
- ✅ Independent of client apps  

---

### Important Difference:
- ❌ No label recommendations (only automatic application)  
- ✅ Must be tested first using **simulation mode**  

---

# 📊 Supported Content & Limits

---

## SharePoint & OneDrive:
- Supported files:
  - Word (.docx)  
  - Excel (.xlsx)  
  - PowerPoint (.pptx)  

---

### Limitations:
- ❌ Cannot label:
  - Open files  
  - List item attachments  
- ✅ Max:
  - 25,000 files/day  
  - 100 policies per tenant  

---

## Exchange (Email):

### Behavior:
- ✅ Scans:
  - Email body  
  - Attachments (PDF, Office files)  

---

### Important:
- Label applies to:
  - ✅ Email  
  - ❌ Not directly to attachment  

---

### Encryption:
- If label includes encryption:
  - Attachments inherit encryption from email  

---

# ⚙️ Label Application Rules

---

## Key Restrictions:

- ❌ Cannot relabel:
  - Content already labeled with **higher sensitivity**  
- ❌ Cannot override manual labels  
- ✅ Only **one sensitivity label per item**  

---

## Detection Scope:

### Can detect:
- Document content  
- Email body  
- Headers/footers  

---

### Cannot detect:
- Email subject line  
- Some attachments (depending on method)  

---

# 🔁 Convert Label to Auto-Labeling Policy

---

### When Creating Label:
- If label includes:
  - ✅ Sensitive information types → Policy option available  
  - ❌ Only trainable classifiers → No auto-policy option  

---

### Policy Creation:
- Automatically populated values  
- Can be edited before deployment  

---

### Default Scope:
- All:
  - SharePoint  
  - OneDrive  
  - Exchange  

---

# 🧪 Simulation Mode (Critical Step)

---

## Why Simulation Mode:
- ✅ Test policy without applying labels  
- ✅ Identify false positives  
- ✅ Refine conditions  

---

## Key Facts:
- ⏱️ Takes ~12 hours per run  
- 📧 Sends results via notification email  
- 🔢 Max:
  - 1,000,000 matched files  

---

## Simulation Workflow:

1. Create policy  
2. Run simulation  
3. Review results  
4. Adjust rules  
5. Repeat if needed  
6. Deploy in production  

---

## Benefits:
- Prevents incorrect labeling  
- Ensures policy accuracy  

---

# 📈 Best Practice Rollout Approach:

1. Start:
   - Small scope (e.g., one SharePoint site)  
2. Validate results  
3. Expand gradually  
4. Deploy across organization  

---

# 🔐 Interaction with Other Policies

---

## With DLP / Mail Flow Rules:
- If label includes encryption:
  - ✅ Overrides IRM settings  
- If label doesn’t:
  - ✅ Both policies apply  

---

# ✅ Example Scenario:

### Goal:
Protect documents with credit card data  

---

### Setup:
- Label:
  - “Confidential”  
- Condition:
  - Credit card numbers  

---

### Behavior:
- File detected → Label applied automatically  
- Email detected → Label applied + encrypted  

---

# ⭐ Key Benefits:

- ✅ Eliminates reliance on users  
- ✅ Consistent classification enforcement  
- ✅ Scales across all data locations  
- ✅ Improves compliance and security  

---

# ⚠️ Key Considerations:

- Always test with simulation mode  
- Ensure labeling prerequisites are enabled  
- Monitor limits (files/day, policies)  
- Combine with DLP for full protection  

---

# 🔑 Key Takeaway:

Automatic sensitivity labeling enables organizations to:
- Detect sensitive content automatically  
- Apply protection consistently  
- Scale data classification across Microsoft 365  

➡️ By combining **client-side guidance and service-side automation**, organizations achieve **accurate, efficient, and enterprise-wide data protection**
