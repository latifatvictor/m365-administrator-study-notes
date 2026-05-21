## Create a Custom DLP Policy from a Template – Summary

### Overview:
- The **easiest way to create a DLP policy** in Microsoft Purview is to use a **built-in template**
- Microsoft provides **40+ predefined templates** for common scenarios:
  - Financial data  
  - Healthcare data  
  - Privacy/PII  
- Templates can be:
  - ✅ Used as-is  
  - ✅ Fully customized  

---

## Why Use Templates:
- ✅ Fast deployment  
- ✅ Preconfigured rules (conditions + actions)  
- ✅ Based on regulatory standards  
- ✅ Reduce design complexity  

---

## What You Can Customize:
- Add/remove sensitive info types  
- Adjust detection thresholds  
- Modify rule actions (block, notify, audit)  
- Allow user override with justification  
- Choose who receives alerts  

---

## Permissions Required:

### To Create Policies:
- Must have:
  - ✅ **DLP Compliance Management role**

---

### Setup Permissions:
1. Create Microsoft 365 group (compliance team)
2. Create role group in Purview
3. Assign:
   - DLP Compliance Management role
4. Add members  

---

### Optional Role:
- View-only access:
  - **View-Only DLP Compliance Management**

---

## Available Roles:
- Information Protection Admin  
- Information Protection Analyst  
- Information Protection Investigator  
- Information Protection Reader  

---

## Steps to Create a DLP Policy from a Template:

---

### Step 1: Open Portal
- Go to:
  - Microsoft Purview compliance portal  
- Navigate:
  - Data Loss Prevention → **Policies**

---

### Step 2: Start Policy Wizard
- Click:
  - **+ Create policy**

---

### Step 3: Choose Template
- Select:
  - Category (e.g., Financial, Health)  
- Pick template:
  - Based on sensitivity type  
- Review description  
- Click **Next**

---

### Step 4: Name Policy
- Provide a unique name  
⚠️ Cannot rename later  

---

### Step 5: Choose Locations
Select where policy applies:

- Exchange email  
- SharePoint sites  
- OneDrive accounts  
- Teams messages  

---

#### Control Scope:
- Entire location → enable/disable  
- Specific resources → include/exclude  

---

### Step 6: Define Policy Settings

Choose one:

- ✅ Review default template settings  
- ✅ Customize advanced rules  

---

### Step 7: Configure Sensitive Data (Info to Protect)
- Review:
  - Sensitive info types  
  - Detection rules  
- Modify if needed  

---

### Step 8: Configure Protection Actions
Choose actions such as:
- 🚫 Block sharing  
- ⚠️ Show policy tips  
- 📧 Send alerts  
- 🔓 Allow override  

---

### Step 9: Customize Access & Overrides
- Configure:
  - Who can override  
  - Notification behavior  

---

### Step 10: Select Policy Mode

Choose:
- ✅ Test mode (recommended)  
- ✅ Turn on immediately (enforce)  
- ✅ Keep off  

---

### Step 11: Review & Create
- Verify all settings  
- Click **Submit**  

---

## Policy Deployment Best Practice:

### Recommended Flow:
1. Test mode (no enforcement)  
2. Test mode (with alerts & tips)  
3. Full enforcement  

---

## Example Scenario:

### Goal:
- Protect financial data  

### Template Used:
- Financial data template  

### Configuration:
- Locations:
  - Exchange + OneDrive  
- Conditions:
  - Credit card numbers detected  
- Actions:
  - Block external sharing  
  - Notify admin  
- Mode:
  - Test first  

---

## Key Considerations:
- Templates are starting points → always refine  
- Location selection affects:
  - Available rules  
  - Actions  
- Policies sync across all workloads automatically  

---

## Best Practices:
- ✅ Start with templates for speed  
- ✅ Customize for business needs  
- ✅ Use test mode before enforcement  
- ✅ Involve stakeholders in design  
- ✅ Continuously monitor and refine  

---

## Key Takeaway:
Creating a DLP policy from a template provides a **fast, structured way to protect sensitive data**, while still allowing:
- Full customization  
- Flexible enforcement  
- Ongoing optimization  

➡️ Templates help organizations **quickly implement effective DLP controls with minimal effort while maintaining flexibility for advanced configurations**
