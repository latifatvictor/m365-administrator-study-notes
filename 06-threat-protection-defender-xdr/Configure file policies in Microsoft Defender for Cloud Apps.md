## File Policies in Microsoft Defender for Cloud Apps Summary

### Overview:
- File policies define **user behavior and data handling rules in the cloud**
- Detect:
  - Risky behavior
  - Data exposure
  - Policy violations
- Apply **automated remediation actions**

---

## How File Policies Work:
- Continuously scan cloud environments
- Use 3 key components:
  1. **Content inspection** (predefined templates or custom expressions)
  2. **Context filters**:
     - User roles
     - File metadata (type, access level)
     - Sharing level (internal/external/public)
  3. **Governance actions** (remediation)

---

### Key Behavior:
- Only **first triggered policy action is applied**
- Policies monitor:
  - Existing files (at rest)
  - Newly created files
- Alerts and reports provide visibility

---

## Types of Policies:
- **Activity policy** → monitors user actions  
- **Anomaly detection policy** → detects unusual behavior  
- **OAuth app policy** → manages app permissions  
- **Malware detection policy** → detects malicious files  
- **File policy** → scans files for sensitive data (**DLP focus**)  
- **Access policy** → controls login access  
- **Session policy** → controls user sessions  
- **App discovery policy** → detects new apps  
- **Cloud discovery anomaly policy** → detects unusual app usage  

---

## Risk Areas Covered:
- Access control (who, where, how)  
- Compliance (regulated data exposure)  
- Configuration changes  
- Shadow IT discovery  
- Data Loss Prevention (DLP)  
- Privileged account monitoring  
- Sharing control (internal/external)  
- Threat detection (suspicious activity)

---

## Example File Policies:
- Detect publicly shared files  
- Alert on files containing company name shared externally  
- Monitor sharing with specific domains (e.g., competitors)  
- Quarantine inactive shared files  
- Detect sensitive file extensions  
- Alert on unauthorized user sharing  

---

## Creating a File Policy (Steps):
1. Go to **Control → Policies → Information protection**
2. Select **+Create policy → File policy**
3. Configure:
   - Policy name & severity  
   - Category (e.g., DLP)  
   - Filters:
     - File type, sharing level, users, folders  
   - Inspection method:
     - Built-in DLP or Data Classification Services  
   - Content rules:
     - Preset or custom expressions  
   - Governance actions:
     - Quarantine, remove sharing, apply labels  

---

## Best Practices:
- Use **narrow filters** to avoid false positives  
- Test with **preview results** before enabling  
- Be cautious with governance actions (can impact access)  
- Monitor matches via:
  - "Matching now"
  - History (last 6 months)

---

## Key Takeaway:
File policies provide **automated, continuous data protection in cloud apps**, combining **content inspection, contextual filtering, and remediation actions** to prevent data leaks and enforce compliance.
