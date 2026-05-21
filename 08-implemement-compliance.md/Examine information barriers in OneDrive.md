## Information Barriers in OneDrive – Microsoft Purview Summary

### Overview:
- Microsoft Purview Information Barriers (IB) control **access and sharing of content in OneDrive**
- Used to:
  - Prevent unauthorized collaboration  
  - Enforce regulatory compliance (finance, legal, government)  
- IB policies are automatically applied to OneDrive when enabled  

---

## What IB Controls in OneDrive:
- ✅ Access to OneDrive sites and files  
- ✅ Sharing of files and folders  
- ✅ Collaboration between users  

---

## Information Barrier (IB) Modes in OneDrive:

### 1. Open Mode
- Default for **non-segmented users**
- No IB restrictions applied  
- Files can be shared based on normal sharing settings  

---

### 2. Owner Moderated Mode
- Allows controlled collaboration with incompatible users  
- Restrictions:
  - ❌ No “Anyone” links  
  - ❌ No company-wide links  
- ✅ Only the site owner can:
  - Share content  
  - Grant access  

---

### 3. Explicit Mode
- Default for **segmented users**
- Strongest restriction

#### Rules:
- ❌ No “Anyone” links  
- ❌ No company-wide links  
- ✅ Sharing only allowed with:
  - Users in the **same segment**  

---

### 4. Inferred Mode
- Allows sharing with:
  - ✅ Same segment users  
  - ✅ Unsegmented users  

#### Rules:
- ❌ No “Anyone” links  
- ❌ No company-wide links  

---

## Sharing Behavior by Mode:

| Mode | Sharing Allowed |
|------|----------------|
| Open | Anyone based on settings |
| Owner Moderated | Controlled by owner, IB-enforced |
| Explicit | Same segment only |
| Inferred | Same segment + unsegmented users |

---

## Access Rules:

### Open Mode:
- Access granted only if:
  - Owner shares content  

---

### Owner Moderated:
- Access requires:
  - Owner permission  

---

### Explicit:
- Requires:
  - Matching segment  
  - File shared explicitly  

---

### Inferred:
- Segmented users:
  - Must match segment + shared access  
- Unsegmented users:
  - Can access if granted permission  

---

## Key Example (Contoso):

Segments:
- HR  
- Sales  
- Research  

Policy:
- ❌ Block Sales ↔ Research  

### Result:

| User Type | Access |
|----------|--------|
| HR | HR only |
| Sales | Sales + HR |
| Research | Research + HR |
| Non-segment | Open access |

---

## Enabling IB for OneDrive:

### Step:
```powershell
Set-SPOTenant -InformationBarriersSuspension $false
