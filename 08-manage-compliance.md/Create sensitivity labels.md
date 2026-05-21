## Create Sensitivity Labels – Microsoft Purview Summary

### Overview:
Sensitivity labels are the **foundation of Microsoft Purview Information Protection**.  
To implement them, you must:
1. ✅ Create and configure labels  
2. ✅ Organize and prioritize them  
3. ✅ Publish them via label policies  

---

# 🧩 1. Where to Create Labels

### In Microsoft Purview:
- Go to:
  - **Information protection → Labels**
- Click:
  - **+ Create a label**

---

# 🛠️ 2. Create a New Sensitivity Label (Step-by-Step)

---

## Step 1: Define Label Details
Provide:

- ✅ **Name** (internal reference)  
- ✅ **Display name** (user-friendly)  
- ✅ **Description for users** (guidance)  
- ✅ **Description for admins** (optional)  

---

### Best Practices:
- Use simple names:
  - Public  
  - General  
  - Confidential  
  - Highly Confidential  
- Add clear descriptions to guide users  

---

## Step 2: Define Label Scope

### Choose where label applies:

---

### ✅ Files & Emails
- Applies to:
  - Word, Excel, PowerPoint  
  - Outlook emails  
- Enables:
  - Encryption  
  - Watermarks  
  - Access controls  

---

### ✅ Groups & Sites (Optional)
- Applies to:
  - Teams  
  - SharePoint  
- Enables:
  - Privacy settings  
  - External sharing restrictions  

---

### ✅ Schematized Data Assets (Optional)
- Applies to:
  - Databases  
  - Azure data sources  

---

⚠️ Important:
- Scope determines:
  - Where label is visible  
  - What settings you can configure  

---

## Step 3: Configure Label Settings

### Available Options (depending on scope):

---

### 🔐 Encryption
- Restrict:
  - Who can access content  
  - What actions they can perform  

---

### 💧 Content Markings
- Add:
  - Watermarks  
  - Headers  
  - Footers  

---

### 🚫 Access Restrictions
- Block:
  - External sharing  
  - Editing or printing  

---

### 🏢 Container Settings (Groups/Sites)
- Control:
  - Privacy (Public/Private)  
  - External user access  
  - Device restrictions  

---

## Step 4: Save Label
- Complete wizard  
- Label is created but **not yet visible to users**  

---

# 🔁 3. Create Additional Labels

Repeat process to build your classification hierarchy:

### Example:
- Public  
- General  
- Confidential  
- Highly Confidential  

---

## ✅ Create Sublabels (Optional)

### Steps:
1. Select parent label  
2. Click:
   - **… (ellipsis) → Add sublabel**  

---

### Example:
- Confidential
  - Finance  
  - HR  
  - Legal  

---

# 🔢 4. Set Label Priority (Critical)

### Rule:
- Top = least restrictive  
- Bottom = most restrictive  

---

### Example Order:
1. Public  
2. General  
3. Confidential  
4. Highly Confidential  

---

### Why It Matters:
- Determines:
  - Label downgrade behavior  
  - Auto-labeling decisions  

---

# ✏️ 5. Edit a Sensitivity Label

### Steps:
1. Select label  
2. Click:
   - **Edit label**  

---

### Notes:
- Changes apply automatically  
- No need to republish policy  
- ⏱️ Changes take up to 24 hours  

---

# ⚠️ 6. Important Considerations

---

## ❗ Labels Are Not Active Until Published
- Users cannot:
  - See or use labels  
- Until:
  - You create a **label policy**

---

## ❗ Avoid Too Many Label Policies
- Best practice:
  - ✅ Use **one policy** where possible  
- Multiple policies only if:
  - Different users need different labels/settings  

---

## ❗ Be Careful When Deleting Labels
- Existing content:
  - May still retain protection  
- Can cause confusion/users issues  

---

# 🔄 7. Deployment Flow

### High-Level Process:

1. Create labels  
2. Configure settings  
3. Organize hierarchy  
4. Publish via label policy  
5. Monitor usage  

---

# ✅ Example Scenario:

### Goal:
Protect sensitive company data  

---

### Labels Created:
- Public  
- General  
- Confidential  
- Highly Confidential  

---

### Configuration:
- Confidential:
  - Header + restricted sharing  
- Highly Confidential:
  - Encryption + watermark  

---

### Deployment:
- Publish to pilot users  
- Expand organization-wide  

---

# ✅ Best Practices:

- ✅ Use clear naming conventions  
- ✅ Keep label structure simple  
- ✅ Set correct label order  
- ✅ Use sublabels for organization  
- ✅ Test labels before full rollout  
- ✅ Avoid unnecessary deletion  

---

# 🔑 Key Takeaway:

Creating sensitivity labels involves:
- Defining classification levels  
- Configuring protection settings  
- Structuring labels correctly  

➡️ Labels become effective only when **published through label policies**, enabling users and services to apply consistent data protection across Microsoft 365
