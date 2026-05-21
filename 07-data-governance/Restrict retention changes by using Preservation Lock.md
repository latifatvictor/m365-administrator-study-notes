## Preservation Lock – Microsoft Purview Summary

### Overview:
- **Preservation Lock** ensures retention policies and label policies **cannot be modified, disabled, or removed**
- Designed to meet strict regulatory requirements (e.g., **SEC Rule 17a-4**)
- Applies to:
  - Retention policies
  - Retention label policies

---

## Purpose:
- Prevent accidental or intentional changes to retention settings  
- Enforce **immutability of compliance policies**  
- Protect against:
  - Rogue administrators  
  - Misconfigurations  
- Ensure data is retained according to legal/regulatory requirements  

---

## Key Characteristics:
- Once enabled:
  - ❌ Cannot disable policy  
  - ❌ Cannot delete policy  
  - ❌ Cannot reduce retention periods  
- ✅ Only allowed changes:
  - Extend retention period  
  - Add locations  
  - Add labels (for label policies)  

---

## Behavior by Policy Type:

### Retention Policy (Locked):
- ✅ Can add locations  
- ✅ Can extend retention duration  
- ❌ Cannot remove locations  
- ❌ Cannot shorten retention period  

---

### Retention Label Policy (Locked):
- ✅ Can add locations  
- ✅ Can add labels  
- ❌ Cannot remove locations  
- ❌ Cannot remove labels  

---

## Important Rule:
👉 You can only make the policy **more restrictive**, never less restrictive  

---

## Critical Warning:
- ❗ **Irreversible action**
- Even **Global Administrators cannot undo it**
- Must carefully validate policy before locking

---

## How to Enable Preservation Lock:

### Step 1: Connect to PowerShell
```powershell
Connect-IPPSSession
