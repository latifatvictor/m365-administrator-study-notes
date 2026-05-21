## Determine a Sensitivity Label’s Scope – Microsoft Purview Summary

### Overview:
When creating a **sensitivity label**, you must define its **scope**, which determines:

1. ✅ **Where the label can be used**  
2. ✅ **What protection settings can be configured**

👉 Scope ensures labels are applied only where relevant (e.g., files vs Teams).

---

# 🔍 1. Label Scope Options

---

## ✅ 1. Items (Default)
Applies to:
- 📄 Files (Word, Excel, PowerPoint, PDF)
- 📧 Emails
- 📅 Meetings (optional refinement)

---

### Refinement Options:
- Files only  
- Emails only  
- Meetings (calendar, Teams meetings, chats)

👉 Example:
- Create a label only for **emails** (exclude files)

---

## ✅ 2. Groups & Sites (Containers)
Applies to:
- Microsoft Teams  
- SharePoint sites  
- Microsoft 365 Groups  

---

### Controls Include:
- Privacy (Public/Private)  
- External sharing  
- Access from unmanaged devices  

⚠️ Note:
- Must enable this feature in tenant first  

---

## ✅ 3. Schematized Data Assets
Applies to:
- Structured data (e.g., databases, Azure data assets)

---

### Examples:
- SQL columns  
- Azure Blob Storage  

---

⚠️ Requires:
- Microsoft Purview Data Map configuration  

---

# ⚙️ 2. Why Scope Matters

### Scope determines:

| Scope Type | Controls Available |
|------------|------------------|
| Items | Encryption, watermark, access restrictions |
| Groups & Sites | Sharing, privacy, device access |
| Data Assets | Data governance controls |

---

👉 Example:
- If you don’t select **Items scope**:
  - ❌ You cannot configure encryption or file protection  

---

# 🚫 Scope Limitations:

- Labels scoped for:
  - **Items only** → cannot be used on Teams/sites  
- Labels scoped for:
  - **Containers only** → cannot be applied to files/emails  

---

# 🧭 3. Label Visibility
- Users only see labels relevant to their scope:
  - File label → appears in Word/Excel/Outlook  
  - Container label → appears in Teams/SharePoint settings  

---

# 🔢 4. Label Priority (Order Matters)

### Important Rule:
- Labels are ordered from:
  - ⬆️ Least restrictive (top)  
  - ⬇️ Most restrictive (bottom)  

---

### Example Order:
1. Public  
2. General  
3. Confidential  
4. Highly Confidential  

---

## Why Priority Matters:

### ✅ Determines:
- Which label is “higher” or “lower” classification  
- What happens when:
  - Users downgrade labels  

---

### Example:
- Downgrading:
  - Highly Confidential → Confidential  
- System can:
  - Require **justification**  

---

### Auto-Labeling Behavior:
- If multiple labels match:
  - ✅ System selects **most restrictive (last in list)**  

---

# 🧩 5. Sublabels (Grouping Labels)

### What Are Sublabels?
- Labels grouped under a **parent label**

---

### Example:
- Parent: **Confidential**
  - Confidential – Finance  
  - Confidential – HR  
  - Confidential – Legal  

---

## Key Rules:

- ✅ Users choose **sublabels only**
- ❌ Parent label **cannot be applied directly**

---

## Important Behavior:
- Sublabels:
  - ✅ Do NOT inherit settings from parent  
- Parent label:
  - ✅ Used only for grouping  

---

⚠️ Important:
- Parent label cannot be:
  - Default label  
  - Auto-applied label  

---

# ✏️ 6. Editing & Deleting Labels

---

## Edit Label:
- Changes apply:
  - ✅ To future use  
- Existing content:
  - ❗ Keeps original applied settings  

---

## Delete Label:
- ❌ Label removed from admin center  
- ✅ Still applied to existing content  

👉 Protection remains enforced  

---

# ✅ Example Scenario:

### Goal:
Protect documents and Teams collaboration space differently

---

### Design:
- Label 1:
  - Scope: Items  
  - Action: Encrypt files  

- Label 2:
  - Scope: Groups & Sites  
  - Action: Restrict external sharing  

---

### Result:
- Files → Protected with encryption  
- Teams → Restricted access settings  

---

# ✅ Best Practices:

- ✅ Choose scope carefully at creation  
- ✅ Separate labels for:
  - Files vs Containers  
- ✅ Maintain logical label hierarchy  
- ✅ Order labels correctly (least → most sensitive)  
- ✅ Use sublabels to simplify user experience  
- ✅ Test label visibility before rollout  

---

# 🔑 Key Takeaway:
A sensitivity label’s scope defines:

- ✅ Where it can be applied  
- ✅ What protections it can enforce  

➡️ Proper scoping ensures labels are:
- Relevant  
- Effective  
- Easy for users to apply  

👉 Combined with priority and sublabels, scope helps build a **clear, scalable data protection strategy in Microsoft Purview**
