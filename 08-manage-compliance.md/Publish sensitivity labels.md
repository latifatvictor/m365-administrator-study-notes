## Publish Sensitivity Labels – Microsoft Purview Summary

### Overview:
- Sensitivity labels become available to users **only after publishing them via a label policy**
- Without a label policy:
  - ❌ Users cannot see or apply labels  
  - ❌ Services cannot enforce protection  

👉 Label policies are the **delivery mechanism** for sensitivity labels

---

# 🧩 1. What Publishing Does

Publishing a label:
- ✅ Makes labels visible in Office apps (Word, Excel, Outlook)
- ✅ Enables users and services to apply labels
- ✅ Applies policy settings (defaults, restrictions, etc.)

---

# 🛠️ 2. Steps to Publish Sensitivity Labels

---

## Step 1: Go to Label Policies
- Navigate:
  - **Microsoft Purview → Information protection → Label policies**

---

## Step 2: Start Policy Creation
- Click:
  - **Publish label**

---

## Step 3: Choose Labels to Publish
- Select:
  - Sensitivity labels to deploy  

---

### ⚠️ Important:
- If selecting a **sublabel**, you must also select its **parent label**

---

## Step 4: Configure Policy Settings

### Settings depend on label scope:
- Files & emails → file/email options shown  
- Groups & sites → container settings shown  

---

### Common Settings:

#### ✅ Assign Users/Groups
- Who can see and use labels  

---

#### ✅ Default Label
- Applied automatically to:
  - New files  
  - Unlabeled emails  

---

#### ✅ Mandatory Labeling
- Require users to:
  - Label documents and emails  

---

#### ✅ Require Justification
- When users:
  - Remove or downgrade labels  

---

#### ✅ Help Link
- Provide:
  - Internal guidance (Learn More link)  

---

## Step 5: Review & Create
- Complete wizard  
- Policy is automatically published  

---

# 🔁 3. Multiple Label Policies

You may create multiple policies if:

- Different users need:
  - Different labels  
  - Different default settings  

---

### Example:
- Finance team → stricter labels  
- General staff → basic labels  

---

# ⚠️ Best Practice:
- ✅ Keep policies minimal  
- Many organizations use:
  - ✅ **One policy for entire organisation**

---

# 🔢 4. Label Policy Priority (Critical)

---

### Ordering:
- Top → Lowest priority  
- Bottom → Highest priority  

---

### When Conflicts Occur:
- ✅ Highest priority policy wins  

---

### Example:
- Policy A → Default = General  
- Policy B (higher priority) → Default = Confidential  

👉 Result:
- Confidential is applied  

---

### Troubleshooting Tip:
- If labels behave unexpectedly:
  - ✅ Check policy order  
  - ✅ Adjust using:
    - Move up / Move down  

---

# ✏️ 5. Editing a Label Policy

---

## To Modify:
1. Select policy  
2. Click:
   - **Edit Policy**

---

## Changes Apply:
- ✅ Automatically (no republish needed)  
- ✅ To all assigned users  

---

# ⏱️ 6. Propagation Time

---

### Standard Timing:
- ⏳ Up to **24 hours**  

---

### Faster Updates (Possible):
- ✅ Web apps (Word, Excel online):
  - May update within hours  

---

### Slower Scenarios:
- ⏳ 24–48 hours when:
  - New groups created  
  - Group membership changes  
  - Network replication delays  

---

# ⚠️ 7. Important Considerations

- ❗ Labels are not usable until published  
- ❗ Policy settings depend on label scope  
- ❗ Policy conflicts resolved by priority  
- ❗ Always wait before troubleshooting (allow 24 hours)  

---

# ✅ Example Scenario

### Goal:
Make sensitivity labels available company-wide

---

### Setup:
- Labels:
  - Public  
  - General  
  - Confidential  
- Policy:
  - Applies to all users  
  - Default label:
    - General  
  - Mandatory labeling:
    - Enabled  

---

### Result:
- Users see labels in apps  
- All documents are labelled  
- Sensitive data is better protected  

---

# ✅ Best Practices:

- ✅ Publish labels using **label policies only**  
- ✅ Limit number of policies  
- ✅ Test with pilot users before full rollout  
- ✅ Ensure correct label and policy ordering  
- ✅ Allow time for propagation before troubleshooting  

---

# 🔑 Key Takeaway:

Publishing sensitivity labels involves:
- Creating a **label policy**
- Assigning labels to users/groups
- Configuring enforcement settings  

➡️ Only after publishing can labels:
- Be seen by users  
- Be applied in apps  
- Enforce data protection  

👉 Label policies transform labels from **definitions into active protection controls**
