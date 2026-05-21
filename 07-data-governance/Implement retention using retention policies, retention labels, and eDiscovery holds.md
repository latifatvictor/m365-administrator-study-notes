## Implement Retention with Policies, Labels, and eDiscovery Holds – Summary

### Overview:
- Organizations use **retention policies, retention labels, and eDiscovery holds** to prevent data deletion
- Each serves a **different purpose**:
  - **Retention settings** → long-term data lifecycle management  
  - **eDiscovery holds** → short-term legal investigations  

---

## 1. Retention Settings (Policies & Labels)

### Purpose:
- Support **compliance and governance**
- Manage data lifecycle:
  - Retain content
  - Delete content
  - Retain then delete

---

### Characteristics:
- ✅ Long-term strategy  
- ✅ Broad scope (locations, content types)  
- ✅ Configurable retention periods  
- ✅ Automatic deletion supported  
- ✅ Low administrative overhead  

---

### Examples:
- Retain emails for 7 years for compliance  
- Delete old files after 5 years  
- Keep specific documents longer using retention labels  

---

## 2. eDiscovery Holds

### Purpose:
- Preserve data for **legal investigations or cases**

---

### Characteristics:
- ✅ Short-term usage  
- ✅ User-specific (custodians)  
- ✅ No automatic deletion  
- ✅ Requires manual start and release  
- ✅ Higher administrative overhead  

---

### Examples:
- Preserve emails of employees involved in litigation  
- Hold documents related to a legal case  

---

## Key Comparison:

| Feature | Retention Settings | eDiscovery Holds |
|--------|------------------|------------------|
| Purpose | Compliance | Legal investigations |
| Duration | Long-term | Short-term |
| Scope | Broad (content/location) | Specific (users/custodians) |
| Configurable period | Yes | No |
| Auto deletion | Yes (optional) | No |
| Management effort | Low | High |

---

## Important Rule:
👉 **eDiscovery holds take precedence over retention settings**

- If both apply:
  - Content **cannot be deleted**
  - Retained until hold is manually removed

---

## Best Practices:

### Use Retention Policies & Labels:
- For **organization-wide governance**
- To automate retention and deletion
- For compliance with regulations

---

### Use eDiscovery Holds:
- For **legal cases and investigations**
- To preserve specific user data
- When data must not be altered or deleted

---

## Replacing Older Features:

### Instead of older tools, use:
- ✅ Retention Policies & Labels

### Replace:
- Exchange MRM (legacy retention)
- Litigation Hold (general usage)
- SharePoint deletion policies
- Information management policies

---

### Why Replace?
- ✅ Unified solution across Microsoft 365  
- ✅ Supports both retention and deletion  
- ✅ Better automation and flexibility  
- ✅ Cross-workload consistency  

---

## Key Takeaway:
- **Retention policies & labels** = long-term, automated data governance  
- **eDiscovery holds** = short-term, legal preservation  
- Combined correctly, they provide **complete control over data lifecycle and legal compliance**
