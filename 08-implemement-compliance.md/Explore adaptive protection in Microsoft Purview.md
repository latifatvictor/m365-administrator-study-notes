## Adaptive Protection in Microsoft Purview – Summary

### Overview:
- **Adaptive Protection** uses **machine learning + insider risk insights** to:
  - ✅ Identify high-risk users  
  - ✅ Automatically apply protection controls  
  - ✅ Adjust security policies dynamically  

👉 It integrates:
- Insider Risk Management  
- Data Loss Prevention (DLP)  
- Microsoft Entra Conditional Access  

---

## Key Capabilities:

---

### 1. Context-Aware Detection
- Uses AI/ML to analyze:
  - User behavior  
  - Data activity  
- Identifies:
  - High-risk actions  
  - Insider threats  

---

### 2. Dynamic Controls
- Automatically applies policies based on risk level:
  - High-risk → strict controls  
  - Low-risk → minimal restrictions  

✅ Ensures:
- Security without harming productivity  

---

### 3. Automated Mitigation
- Reduces manual intervention  
- Automatically:
  - Applies DLP controls  
  - Enforces Conditional Access  

---

## How Adaptive Protection Works:

1. Insider Risk Management evaluates user behavior  
2. Assigns **risk level** (Minor, Moderate, Elevated)  
3. Adaptive Protection:
   - Applies **DLP policies**  
   - Applies **Conditional Access controls**  
4. Adjusts policies dynamically as risk changes  

---

## Risk Levels:

### 1. Elevated Risk (High)
- Examples:
  - Multiple high-severity alerts  
  - Repeated risky behavior  
- Actions:
  - Block data sharing  
  - Block application access  

---

### 2. Moderate Risk
- Examples:
  - Medium severity alerts  
  - Multiple exfiltration activities  
- Actions:
  - Restrict access  
  - Increase monitoring  

---

### 3. Minor Risk (Low)
- Examples:
  - Low severity activity  
- Actions:
  - Show policy tips  
  - Educate users  

---

### Key Note:
- Risk levels are based on:
  - **Insights (aggregated activity + severity)**  
  - Not just single events  

---

## Customizing Risk Levels:
- Organizations can:
  - Define thresholds  
  - Customize indicators  
  - Adjust severity triggers  

---

## Example Use Cases:

### DLP Integration:
- Minor/Moderate:
  - ⚠️ Show warnings  
- Elevated:
  - 🚫 Block sharing of sensitive data  

---

### Conditional Access:
- Minor:
  - Require Terms of Use  
- Moderate:
  - Restrict app access  
- Elevated:
  - Block all access  

---

## Integration with DLP:
- Automatically:
  - Applies DLP policies based on risk level  
- Adjusts:
  - Policy enforcement as risk changes  

✅ Example:
- User becomes high risk → stricter DLP rules applied  

---

## Setup Options:

---

### 1. Quick Setup (Recommended for beginners)
- Automatically configures:
  - Insider risk settings  
  - Risk levels  
  - DLP policies  
  - Conditional Access policy  

---

#### What It Creates:
- Insider risk policy (Data leaks)
- 2 DLP policies:
  - Endpoint DLP  
  - Teams/Exchange DLP  
- Conditional Access policy:
  - Blocks elevated risk users  

---

#### Default Behavior:
- Elevated risk → Block  
- Moderate/Minor → Audit  

---

#### Notes:
- Runs initial policies in **audit/test mode**
- Full setup may take up to **72 hours**

---

### 2. Custom Setup
- Full control over:
  - Risk levels  
  - Policies  
  - Conditions  
- Best for:
  - Mature environments  
  - Pre-configured DLP/Insider Risk setups  

---

## Adaptive Protection Workflow:

1. User performs risky activity  
2. Insider risk assigns risk score  
3. Adaptive protection evaluates risk level  
4. System applies:
   - DLP controls  
   - Access restrictions  
5. Adjusts automatically as behavior changes  

---

## Benefits:
- ✅ Proactive risk detection  
- ✅ Automated response  
- ✅ Reduced admin workload  
- ✅ Improved compliance  
- ✅ Maintained productivity for low-risk users  

---

## Important Notes:
- Requires:
  - Insider Risk Management + DLP + Conditional Access  
- Availability:
  - Supported regions only  
- Policies update dynamically in real time  

---

## Key Takeaway:
Adaptive Protection provides **intelligent, automated risk-based security** by:
- Continuously evaluating user behavior  
- Dynamically enforcing policies  
- Balancing security with productivity  

➡️ It enables organizations to **respond faster and smarter to insider threats using AI-driven controls**
