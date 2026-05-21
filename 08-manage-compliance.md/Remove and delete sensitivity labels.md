## Remove and Delete Sensitivity Labels – Microsoft Purview Summary

### Overview:
In Microsoft Purview, there are two different actions you can take when managing sensitivity labels:
- ✅ **Remove a label from a policy**
- ❌ **Delete a label entirely**

👉 These actions have very different impacts on users and data.

---

# 🔄 1. Removing a Label from a Label Policy

### What It Means:
- You **unpublish the label** from selected users/groups  
- The label:
  - ❌ No longer appears in Office apps  
  - ✅ Still exists in the system  

---

## ✅ Effects:

### For Users:
- Label disappears from:
  - Word, Excel, Outlook label list  

---

### For Existing Content:
- ✅ Label **remains applied**
- ✅ Protection (encryption, restrictions) **still enforced**

---

### Example:
- A file labeled “Confidential”:
  - Continues to show label (status bar)  
  - Continues to be protected  

---

## ✅ Why Use This Approach:
- Safer option  
- ✅ Reversible (you can re-add the label later)  
- ✅ Ideal for:
  - Testing  
  - Gradual rollout  

---

# ❌ 2. Deleting a Sensitivity Label

### What It Means:
- Label is **permanently removed from the system**

---

## 🚨 Effects (Important):

---

## 🔐 A. If the Label Used Encryption:

- Protection template is:
  - ✅ **Archived (not deleted)**  

---

### Result:
- Existing encrypted files:
  - ✅ Can still be opened  
- However:
  - ❌ Cannot reuse the same label name (template conflict)  

---

⚠️ Warning:
- Deleting protection templates via PowerShell:
  - ❗ Risky  
  - ❗ May break access to old encrypted files  

---

## 📄 B. Files in SharePoint / OneDrive:

If sensitivity labels for Office files are enabled:

---

### Behavior:
- ❌ Label name disappears  
- ❌ Not visible in apps or SharePoint columns  

---

### Encryption:
- If environment supports processing:
