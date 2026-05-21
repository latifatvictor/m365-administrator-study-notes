## Define the Scope of a Retention Policy – Summary

### Overview:
When creating a **retention policy or retention label policy**, you must define its scope as either:
- **Adaptive scope (dynamic)**
- **Static scope (fixed)**

---

## 1. Adaptive Scope (Dynamic)

### Definition:
- Uses **queries based on attributes** (e.g., Microsoft Entra ID properties)
- Membership is **dynamic** and updates automatically (daily)

---

### Example:
- Policy targets users with:
  - Job title = "Executive"
- Applies to:
  - Exchange mailboxes
  - OneDrive accounts  
- ✅ Automatically includes new executives without manual updates

---

### Advantages:
- ✅ **No manual updates required** (auto-adjusts to changes)
- ✅ **No limit on items per policy**
- ✅ **More flexible targeting**
  - By department, location, role, etc.
- ✅ Reduces need for maintaining groups
- ✅ Can handle dynamic environments efficiently
- ✅ Supports advanced scenarios (e.g., inactive mailboxes)

---

### Considerations:
- ❌ Not supported for:
  - Exchange public folders  
  - Skype for Business public folders  
- ❌ Does not support **Preservation Lock** (currently)

---

## 2. Static Scope (Fixed)

### Definition:
- Uses **manual selection**
- Scope options:
  - All instances (org-wide)
  - Include specific users/sites
  - Exclude specific users/sites

---

### Example:
- Select:
  - Executive user group for Exchange  
  - Manually specify OneDrive URLs  
- ❌ Requires manual updates when users change

---

### Advantages:
- ✅ **Simple setup** for small or stable environments
- ✅ Ideal when:
  - Few users or sites
  - Minimal changes expected
- ✅ Required for unsupported adaptive locations

---

### Limitations:
- ❌ Requires ongoing maintenance  
- ❌ Hard to scale  
- ❌ Risk of missing updates (e.g., user changes, URL changes)  
- ❌ Less flexible targeting  

---

## Key Differences:

| Feature | Adaptive Scope | Static Scope |
|--------|--------------|--------------|
| Membership | Dynamic | Fixed |
| Updates | Automatic | Manual |
| Scalability | High | Limited |
| Setup complexity | Medium | Simple initially |
| Maintenance | Low | High over time |
| Targeting flexibility | Advanced (query-based) | Limited |

---

## When to Use Each:

### Use Adaptive Scope:
- Large or growing organizations  
- Frequent user/title/location changes  
- Need dynamic, rule-based targeting  

---

### Use Static Scope:
- Small, stable environments  
- Few users/sites to manage  
- Workloads not supported by adaptive scopes  

---

## Key Takeaway:
- **Adaptive scopes** provide **automation, scalability, and flexibility**
- **Static scopes** provide **simplicity for small or stable environments**
- For most modern organizations, **adaptive scopes are the preferred approach** for efficient and scalable data governance
