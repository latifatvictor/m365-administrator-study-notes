## Create Insider Risk Management Policies – Summary

### Overview:
- Insider Risk Management policies use **templates** to define:
  - Risk indicators  
  - Triggering events  
  - Risk scoring models  
- ✅ Each policy **must use a template**
- ✅ Up to **5 policies per template**

---

## Key Concepts:

### 1. Triggering Events
- Define when a user becomes **active for monitoring**
- Example:
  - Resignation date  
  - DLP alert  
- ⚠️ Without triggering events:
  - User activity is NOT evaluated (unless manually added)

---

### 2. Prerequisites
- Required integrations for policies to work:

| Template Type | Requirement |
|--------------|-------------|
| Data leaks | DLP policies |
| Security violations | Defender for Endpoint |
| Departing/disgruntled users | HR connector |
| Patient data misuse | Healthcare/Epic connector |

---

## Prioritizing Content:
- Increase **risk score + alert severity**

### Options:
- SharePoint sites  
- Sensitive info types  
- Sensitivity labels  
- File extensions (up to 50)

✅ Example:
- Prioritize a confidential SharePoint site → higher alert probability  

---

## Sequence Detection:

### Purpose:
- Detect **patterns of risky behavior** (not just single actions)

### Supported Templates:
- Data theft (departing users)  
- Data leaks (all variants)

---

### Activity Categories:
1. **Collection** → downloads  
2. **Exfiltration** → sharing/sending data  
3. **Obfuscation** → hiding activity  
4. **Clean-up** → deleting evidence  

✅ Helps:
- Detect advanced insider threats  

---

## Steps to Create a Policy:

### Step 1: Start Policy Wizard
- Go to:
  - Purview → Insider Risk Management → **Policies → Create Policy**

---

### Step 2: Choose Template
- Select:
  - Data leaks, security violations, etc.
- Review:
  - Prerequisites  
  - Triggering events  

---

### Step 3: Name & Description
- Provide:
  - Policy name (cannot be changed)  
  - Optional description  

---

### Step 4: Define Scope
- Choose:
  - All users OR specific users/groups  
- Add:
  - Priority user groups (if required)

---

### Step 5: Set Content Priority (Optional)
- Select:
  - SharePoint sites  
  - Sensitivity labels  
  - Sensitive info types  
  - File extensions  

---

### Step 6: Configure Triggering Events
- Option:
  - DLP policy trigger  
  - Custom activity indicators  

---

### Step 7: Set Thresholds
- Choose:
  - Default thresholds  
  - Custom thresholds  

✅ Controls:
- Alert sensitivity  

---

### Step 8: Select Policy Indicators
- Choose:
  - Activities to monitor  
- Optional:
  - Risk score boosters  
  - Sequence detection  
  - Cumulative exfiltration  

---

### Step 9: Configure Indicator Thresholds
- Default OR custom thresholds for:
  - Each indicator  

---

### Step 10: Review & Deploy
- Review:
  - Settings  
  - Warnings  
- Select:
  - **Submit** → Policy activates immediately  

---

## Immediately Start Scoring Users:

### Use Case:
- Need to monitor users **without triggering events**

---

### Actions:
- Manually add users:
  - Duration: **5–30 days**
  - Provide reason  
- Import users via:
  - CSV file  

---

### Scenarios:
- Security incidents  
- High-risk users  
- Missing HR/DLP signals  

✅ Benefit:
- Immediate monitoring without waiting for triggers  

---

## Key Best Practices:
- ✅ Configure prerequisites first (DLP, HR, Defender)
- ✅ Use priority content to focus detection
- ✅ Enable sequence detection for deeper insights
- ✅ Start with default thresholds → refine later
- ✅ Test policies with small user groups

---

## Key Takeaway:
Creating Insider Risk Management policies involves:
- Defining **triggers, indicators, and scope**
- Leveraging **templates and integrations**
- Fine-tuning **risk scoring and thresholds**

➡️ This enables organizations to **proactively detect, prioritize, and respond to insider threats effectively**
