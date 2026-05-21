## Design a Custom DLP Policy – Microsoft Purview Summary

### Overview:
Designing a custom DLP policy ensures **accurate, effective, and business-aligned data protection**.  
Rather than relying on trial and error, organizations should:
- ✅ Clearly define business needs  
- ✅ Document intent  
- ✅ Map requirements to configuration  

---

## 1. What a DLP Policy Does:
- Detects sensitive data using:
  - Keywords  
  - Regex patterns  
  - Proximity analysis  
  - Machine learning  
- Protects data across:
  - Microsoft 365 (Exchange, SharePoint, Teams, OneDrive)  
  - Endpoints (Windows/macOS)  
  - Cloud apps  
  - On-premises  

---

## 2. Key Design Principle:
👉 Always start with a **Policy Intent Statement**

---

## 3. Define Policy Intent:

### Purpose:
- Summarizes the **business goal of the policy**
- Drives alignment across stakeholders  

---

### Example:
> “Protect healthcare data (HIPAA) stored in OneDrive/SharePoint and prevent sharing via Teams or external users.”

---

### Intent Must Answer 4 Questions:
1. What to monitor?  
2. Where to monitor?  
3. What conditions trigger the policy?  
4. What actions should be taken?  

---

## 4. Map Intent to Policy Configuration:

### Example Mapping:

---

#### 1. What to Monitor:
- Data type:
  - Sensitive info (e.g., HIPAA, credit cards)  
- Use:
  - Built-in templates OR custom definitions  

---

#### 2. Where to Monitor:
- Locations:
  - Exchange  
  - SharePoint  
  - OneDrive  
  - Teams  
  - Endpoints  

---

#### 3. Conditions:
- Trigger when:
  - Sensitive data is detected  
  - Data is shared externally  
- Consider:
  - Confidence level  
  - Number of occurrences  

---

#### 4. Actions:
- Examples:
  - 🚫 Block sharing  
  - ⚠️ Show policy tip  
  - 📧 Send notification  
  - 🔓 Allow override  

---

## 5. Policy Design Process:

---

### Step 1: Plan (Foundation)
- Identify stakeholders  
- Define sensitive data categories  
- Align with business objectives  

---

### Step 2: Understand DLP Capabilities
- Review:
  - DLP components  
  - Templates  
  - Conditions & actions  

---

### Step 3: Develop Policy Intent Statement
- Collaborate with stakeholders  
- Ensure clarity and alignment  

---

### Step 4: Align with Strategy
- Ensure policy fits overall:
  - DLP roadmap  
  - Security strategy  

---

### Step 5: Choose Template
- Options:
  - Predefined (Financial, Health, Privacy)  
  - Custom policy  

---

### Step 6: Map Intent → Configuration
- Translate:
  - Business requirements  
  - Into technical controls  

---

### Step 7: Fill Gaps
- Identify missing requirements  
- Validate with stakeholders  

---

### Step 8: Document Policy Design
- Include:
  - Scope  
  - Conditions  
  - Actions  
  - Exceptions  

---

### Step 9: Create Draft Policy
- Implement in:
  - Simulation/test mode  

---

## 6. Important Design Considerations:

### Naming Convention
- ❗ Policies cannot be renamed after creation  
- Define naming standard upfront  

---

### Location Impact
- Selected locations determine:
  - Available conditions  
  - Available actions  

---

### Iteration & Review
- Design → Review → Adjust → Implement  

---

## 7. Best Practices:
- ✅ Start with clear business intent  
- ✅ Use predefined templates where possible  
- ✅ Involve stakeholders early  
- ✅ Document everything  
- ✅ Avoid “trial-and-error only” approach  
- ✅ Test before enforcement  

---

## 8. Example End-to-End Design:

### Intent:
- Protect financial data externally  

---

### Configuration:
- Monitor:
  - Credit card numbers  
- Locations:
  - Email, OneDrive, SharePoint  
- Conditions:
  - External sharing detected  
- Actions:
  - Block + notify + allow override  

---

## Key Takeaway:
Designing a custom DLP policy requires:
- Clear intent  
- Strong stakeholder input  
- Structured mapping from business need → technical controls  

➡️ A well-designed policy leads to **accurate detection, effective protection, and minimal disruption to business operations**
