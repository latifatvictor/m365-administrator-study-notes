## Retention Policies vs Retention Labels – Comparison Summary

### Core Similarities:
- Both support:
  - ✅ Retain-only
  - ✅ Delete-only
  - ✅ Retain then delete
- Both:
  - Apply automatically
  - Support key workloads (Exchange, SharePoint, OneDrive, Microsoft 365 Groups)
  - Provide auditing of admin activity

---

## Key Differences:

### Retention Policies
- Apply at **container level** (mailboxes, sites)
- ✅ Easy bulk deployment  
- ✅ Support more workloads (Teams, Yammer, Skype, public folders)  
- ✅ No user interaction required  
- ❌ No manual application  
- ❌ Do not persist when content is moved  
- ❌ No advanced automation (conditions, classifiers)  
- ❌ Cannot mark items as records  

---

### Retention Labels
- Apply at **item level** (file, email, document)
- ✅ Highly flexible and granular  
- ✅ Can be applied:
  - Manually
  - Automatically (conditions, classifiers, keywords)
- ✅ Persist within Microsoft 365 when content moves  
- ✅ Can:
  - Mark items as records  
  - Trigger event-based retention  
  - Support disposition review  
  - Provide proof of deletion  
- ✅ Enable end-user interaction  
- ✅ Enable advanced automation and lifecycle workflows  

---

## Feature Comparison (Quick View):

| Capability | Retention Policies | Retention Labels |
|-----------|------------------|------------------|
| Scope | Container level | Item level |
| Automation | Basic | Advanced (AI, rules, conditions) |
| Manual application | ❌ | ✅ |
| End-user interaction | ❌ | ✅ |
| Moves with content | ❌ | ✅ (within M365) |
| Record management | ❌ | ✅ |
| Event-based retention | ❌ | ✅ |
| Disposition review | ❌ | ✅ |
| Proof of deletion | ❌ | ✅ |

---

## Best Practice: Use Both Together

### Why?
- Policies = **baseline governance**
- Labels = **granular control & exceptions**

---

## Example Scenarios:

### 1. Override Automatic Deletion
- Policy: Delete OneDrive data after 5 years  
- Label: Retain specific documents indefinitely  

---

### 2. Longer Retention for Specific Content
- Policy: Retain SharePoint content for 5 years  
- Label: Retain selected documents for 10 years  

---

### 3. Shorter Retention for Specific Data
- Policy: Delete emails after 10 years  
- Label: Delete project-related emails after 1 year  

---

## Deployment Notes:
- Policies & labels can take up to **7 days** to apply  
- Use PowerShell to retry failed deployments:
```powershell
Set-RetentionCompliancePolicy -Identity <policy name> -RetryDistribution
