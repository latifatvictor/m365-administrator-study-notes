## Implement Data Classification in Microsoft 365 – Summary

### Overview:
- Microsoft 365 uses **data classification** to:
  - ✅ Discover sensitive data  
  - ✅ Classify and label content  
  - ✅ Monitor usage and activity  
- Uses a **zero change management approach**:
  - Scans data *before policies are applied*  
  - Provides insight without disrupting users  

---

## Key Objectives:
- Understand:
  - What sensitive data exists  
  - Where it is stored  
  - How it’s being used  
- Enable:
  - Protection  
  - Governance  
  - Compliance  

---

## Core Capabilities:

### 1. Discover Data
- Automatically scan:
  - Emails  
  - Documents  
  - Files across Microsoft 365  

---

### 2. Classify Data
- Apply classifications using:
  - Sensitivity labels  
  - Retention labels  
  - Sensitive information types  
  - Trainable classifiers  

---

### 3. Protect Data
- Enforce:
  - Encryption  
  - Access control  
  - Data handling rules  

---

### 4. Govern Data
- Control:
  - Retention  
  - Deletion  
  - Lifecycle management  

---

## Microsoft Purview Data Classification Dashboard:

### Provides Visibility Into:
- Number of sensitive items  
- Types of sensitive information  
- Top sensitivity labels used  
- Top retention labels used  
- User activity on sensitive data  
- Data locations (Exchange, SharePoint, OneDrive, endpoints)  

---

## Key Tools in Data Classification:

---

### 1. Overview Page
- Shows:
  - Top sensitive info types  
  - Label usage trends  
  - Classification activity insights  

---

### 2. Classifiers

#### a. Trainable Classifiers
- Use machine learning  
- Detect:
  - Resume  
  - Source code  
  - Offensive content  
- Can create custom classifiers  

---

#### b. Sensitive Information Types (SIT)
- Detect:
  - Credit cards  
  - SSNs  
  - Bank data  
- Built-in or custom  

---

#### c. Exact Data Match (EDM)
- Matches:
  - Exact database values  
- Benefits:
  - Lower false positives  
  - Highly accurate  
  - Supports large datasets  

---

### 3. Content Explorer
- View:
  - Files with sensitive info  
  - Label usage  
- Drill into:
  - Specific documents  
  - Data locations  
- Export results for analysis  

---

### 4. Activity Explorer
- Tracks user activity:
  - File edits  
  - Label changes  
  - Data sharing  
- Filter by:
  - User  
  - Date  
  - Location  
  - Activity type  

---

## Applying Sensitivity Labels:

### Methods:
- ✅ Manual (user applied)  
- ✅ Default (policy-based)  
- ✅ Automatic (based on conditions)  

---

### Example Mapping:

| Classification | Sensitivity Label |
|---------------|------------------|
| Public        | Unrestricted     |
| Internal      | General          |

---

### Note:
- Labels may evolve over time  
- Start simple, refine based on user feedback  

---

## Implementation Approaches:

---

### Small Organizations:
- Use:
  - Simple framework  
- Example:
  - One label per classification level  

---

### Large Organizations:
- More complex:
  - Regional differences  
  - Multiple policies  
- May require:
  - Many labels per classification level  

---

## Continuous Process:

Data classification is **ongoing**, not one-time:

1. Discover data  
2. Classify and label  
3. Monitor usage  
4. Analyze results  
5. Refine policies  

---

## Important Requirements:

- ✅ Enable auditing to track activity  
- ✅ Monitor dashboards regularly  
- ✅ Update classification rules as needed  

---

## Best Practices:
- ✅ Start with built-in classifiers  
- ✅ Use Content Explorer to validate results  
- ✅ Leverage Activity Explorer for monitoring  
- ✅ Train users on classification practices  
- ✅ Regularly review classification insights  

---

## Key Benefits:
- ✅ Better visibility into sensitive data  
- ✅ Improved compliance posture  
- ✅ Reduced risk of data leaks  
- ✅ Stronger data governance  
- ✅ Informed DLP policy design  

---

## Key Takeaway:
Implementing data classification in Microsoft 365 enables organizations to:
- Discover and understand their data  
- Apply appropriate protections  
- Continuously monitor and improve  

➡️ It forms the **foundation for effective data protection, governance, and compliance across Microsoft 365**
