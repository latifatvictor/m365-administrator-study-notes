## Principles of Retention – Microsoft Purview Summary

### Overview:
- Multiple **retention policies and labels** can apply to the same item
- The system evaluates:
  - **Retention duration**
  - **Deletion timing**
- These are calculated **independently**

---

## Key Concept:
👉 The system does NOT choose one policy or label  
👉 It calculates:
- **How long to keep (retain)**
- **When to delete**

---

## Core Principles of Retention:

### 1. Retention Always Wins Over Deletion
- If an item must be retained, it **cannot be deleted**
- Even if a deletion rule exists, it is **suspended**

✅ Example:
- Policy: Delete after 3 years  
- Label: Retain for 5 years  
➡️ Result: Retained for 5 years → then deleted  

---

### 2. Longest Retention Period Wins
- If multiple retention settings exist:
  - The **longest retention period applies**

✅ Example:
- Policy A: Retain 5 years  
- Policy B: Retain 10 years  
➡️ Result: Retain 10 years  

⚠️ Note:
- Start date matters (created vs modified)

---

### 3. Retention Label Deletion Overrides Policy Deletion
- If deletion rules conflict:
  - **Retention label deletion takes precedence**

✅ Example:
- Policy deletes after 10 years  
- Label deletes after 7 years  
➡️ Result: Deleted after 7 years  

---

### 4. Scoped Policies Override Org-Wide Policies
- Specific scope (adaptive/static include) > org-wide policy  

✅ Example:
- Org-wide policy: Delete after 10 years  
- Scoped policy: Delete after 5 years  
➡️ Result: Delete after 5 years  

---

### 5. Shortest Deletion Period Wins (Final Tie-breaker)
- If multiple deletion rules still conflict:
  - **Shortest deletion time applies**

✅ Example:
- Policy A: Delete after 10 years  
- Policy B: Delete after 7 years  
➡️ Result: Delete after 7 years  

---

## Combined Logic Flow:
1. Apply retention rules → keep content  
2. Choose longest retention period  
3. Determine deletion rules:
   - Label > policy  
   - Scoped > org-wide  
   - Shortest deletion time wins  

---

## Retention Period vs Specified Retention:

| Type | Meaning |
|------|--------|
| Item retention period | Specific to individual item |
| Policy retention period | Applies to group of items |

---

## Retention Start Triggers:
- Default → **Created date**  
- Files → **Last modified date**  
- Labels support:
  - When labeled  
  - Event-based (e.g., contract expiry)

---

## Example Scenarios:

### Scenario 1:
- Policy: Delete after 5 years  
- Policy: Retain 3 years then delete  
- Label: Retain 7 years  

➡️ Result:
- Retain = 7 years (longest)  
- Delete = after 7 years  

---

### Scenario 2:
- Org policy: Delete after 10 years  
- Scoped policy: Retain 5 years then delete  
- Label: Retain 3 years then delete  

➡️ Result:
- Retain = 5 years  
- Delete = 3 years (label overrides)  

---

## Special Case:
### eDiscovery / Litigation Hold
- ✅ Overrides all deletion rules  
- Content **cannot be deleted**
- Retention resumes after hold is released  

---

## Key Takeaway:
Retention logic follows clear priorities:
1. **Keep data first (retention wins)**
2. **Keep it for the longest required time**
3. **Apply the strongest *explicit* deletion rule (labels first)**
4. **Resolve conflicts using scope and shortest deletion timing**

➡️ This ensures **compliance, consistency, and data protection** across Microsoft 365.
