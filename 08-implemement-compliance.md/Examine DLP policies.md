## Microsoft Purview DLP Policies – Summary

### Overview:
- A **DLP policy** combines:
  - ✅ Search patterns (sensitive data detection)
  - ✅ Locations (where to apply protection)
  - ✅ Conditions (when to trigger)
  - ✅ Actions (what to do)

👉 Purpose:
- Identify, monitor, and protect sensitive data across Microsoft 365 and beyond

---

## Where DLP Policies Apply:
DLP policies protect data across:

### Microsoft 365:
- Exchange Online (email)
- SharePoint Online
- OneDrive
- Microsoft Teams

### Other locations:
- Endpoints (Windows/macOS)
- On-premises repositories
- Microsoft Cloud App Security
- Power BI

✅ Works across:
- Data at rest  
- Data in motion  
- Data in use  

---

## Core Components of DLP Policies:

---

### 1. Rules
- A policy can contain **multiple rules**
- Each rule:
  - Defines conditions
  - Triggers actions  

---

### 2. Conditions
- Define **when a rule applies**

---

#### Examples:
- Content contains:
  - Credit card numbers
  - Social security numbers
- Data shared:
  - Internally vs externally
- Document properties:
  - Classification labels (e.g., FCI metadata)

---

#### Capabilities:
- Detect **80+ built-in sensitive info types**
- Differentiate:
  - Low risk (internal sharing)
  - High risk (external sharing)

---

### 3. Actions
- Define **what happens when conditions are met**

---

#### Common Actions:
- 🚫 Block access or sharing  
- ⚠️ Show policy tips  
- 📧 Send notifications  
- 🔒 Restrict permissions  
- 📦 Move data to quarantine  

---

#### User Override:
- ✅ Optionally allow:
  - Override with justification  
- ✅ Logged for auditing  

---

## Example Policy Scenario:
- Condition:
  - Email contains credit card numbers  
  - Sent outside organization  
- Action:
  - Block email  
  - Show warning  
  - Notify admin  

---

## DLP Policy Configuration Steps:

---

### 1. Choose Policy Type
- ✅ Use predefined templates:
  - Financial data  
  - Health data  
  - Privacy/PII  
- ✅ Or create custom policy  

---

### 2. Define Scope (Admin Units)
- Scope policies to:
  - Entire organization  
  - Specific users/groups  

---

### 3. Choose Locations
- Select where to apply policy:

| Location | Scope Options |
|----------|--------------|
| Exchange | Distribution groups |
| SharePoint | Sites |
| OneDrive | Accounts |
| Teams | Users/groups |
| Endpoints | Users/groups |
| On-prem | File paths |

---

### 4. Define Conditions
- Customize:
  - Sensitive data types  
  - Sharing behavior  
  - Labels  

---

### 5. Configure Actions
- Choose protection methods:
  - Block  
  - Notify  
  - Audit  
  - Restrict  
  - Tip users  

---

## Policy Deployment:

### Central Policy Store:
- Policies are stored centrally and synced to:
  - Exchange  
  - SharePoint  
  - OneDrive  
  - Teams  
  - Office apps  

✅ Enforcement happens at source  

---

## Simulation Mode vs Enforce Mode:

---

### Simulation Mode (Recommended First):
- ✅ Test policies safely  
- ✅ No enforcement  
- ✅ Generates reports and alerts  

---

### Benefits:
- Identify false positives  
- Fine-tune rules  
- Avoid business disruption  

---

### Enforce Mode:
- ✅ Fully active  
- ✅ Actions applied in real-time  

---

## Simulation Mode Features:
- Dashboard insights  
- Matched items list  
- Policy impact analysis  

---

### Example Use Case:
- Policy v1 → too many false positives  
- Create policy v2 → test in simulation  
- Validate improvements  
- Switch v2 → enforce mode  

---

## Key Tuning Areas:
- Scope (users/locations)  
- Conditions (data detection rules)  
- Sensitivity definitions  
- Exceptions and thresholds  
- Actions severity  

---

## Important Notes:
- ⏱️ Policies take ~1 hour to activate  
- ⏳ Simulation runs up to 15 days  
- 📊 Simulation data retained for 30 days  
- ⚠️ “Stop processing more rules” doesn’t apply in simulation mode  

---

## Best Practices:
- ✅ Start with templates  
- ✅ Use simulation before enforcement  
- ✅ Gradually increase restrictions  
- ✅ Monitor alerts and reports  
- ✅ Train users with policy tips  

---

## Key Takeaway:
DLP policies provide a **flexible and powerful framework** to:
- Detect sensitive data  
- Monitor user activity  
- Automatically enforce protection  

➡️ By combining **conditions, rules, and actions**, organizations can **prevent data leakage while maintaining business productivity**
