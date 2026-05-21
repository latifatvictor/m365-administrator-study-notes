## Information Barriers in SharePoint – Microsoft Purview Summary

### Overview:
- Microsoft Purview Information Barriers (IB) control **access, sharing, and collaboration** in SharePoint
- Used to:
  - Prevent unauthorized access  
  - Restrict collaboration between segments  
  - Enforce compliance in regulated environments  

---

## What IB Controls in SharePoint:
- ✅ Adding users to a site  
- ✅ Access to site and content  
- ✅ Sharing of sites and files  
- ✅ Collaboration between users  

---

## Information Barrier (IB) Modes in SharePoint:

### 1. Open Mode
- Default for sites with **no segments**
- ✅ No IB restrictions  
- Sharing depends on user policy  

---

### 2. Owner Moderated Mode (Preview)
- Used for collaboration between **incompatible segments**
- Only for **non-group connected sites**

#### Rules:
- ❌ No “Anyone” links  
- ❌ No company-wide sharing  
- ✅ Only site owner manages sharing  

---

### 3. Implicit Mode
- Default for **Microsoft Teams-connected sites**
- Access controlled by:
  - ✅ Microsoft 365 group membership  

#### Rules:
- ❌ No “Anyone” links  
- ❌ No company-wide links  
- ✅ Users must be part of the Team  

---

### 4. Explicit Mode
- Used when **segments are applied to a site**

#### Rules:
- ❌ No “Anyone” links  
- ❌ No company-wide links  
- ✅ Only users in matching segments can:
  - Access  
  - Share  
  - Join  

---

## Sharing Behavior by IB Mode:

| Mode | Sharing Rules |
|------|-------------|
| Open | Based on IB policy + sharing settings |
| Owner Moderated | Controlled by owner, IB enforced |
| Implicit | Share only with team members |
| Explicit | Share only with matching segment users |

---

## Access Control Rules:

### Open Mode:
- User must:
  - Have site permission  

---

### Owner Moderated:
- Access requires:
  - Owner approval  

---

### Implicit Mode:
- User must:
  - Be a member of the Microsoft 365 group  

---

### Explicit Mode:
- User must:
  - Match the site's segment  
  - Have site permissions  

⚠️ Non-segment users:
- Cannot access segmented sites  

---

## Example Scenario (Contoso):

Segments:
- HR  
- Sales  
- Research  

Policy:
- ❌ Block Sales ↔ Research  

---

### Outcome:
- HR can collaborate with both  
- Sales and Research:
  - Cannot share content  
  - Cannot access each other’s sites  

✅ Sites can only include **compatible segments**  

---

## Site Creation Behavior:

### Segmented User Creates Site:
- ✅ Site linked to user’s segment  
- ✅ IB mode = Explicit  

---

### Non-Segmented User Creates Site:
- ✅ No segment assigned  
- ✅ IB mode = Open  

---

### Admin Creates Site:
- ✅ No segment assigned initially  
- ✅ IB mode = Open  

---

## Microsoft Teams Integration:
- Teams automatically create SharePoint sites  
- After enabling IB:
  - ✅ Mode = Implicit  
  - ✅ Segments aligned with team members  

---

## Enabling IB in SharePoint & OneDrive:

```powershell
Set-SPOTenant -InformationBarriersSuspension $false
