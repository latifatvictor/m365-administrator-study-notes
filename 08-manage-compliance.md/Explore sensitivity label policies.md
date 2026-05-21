## Sensitivity Label Policies – Microsoft Purview Summary

### Overview:
After creating sensitivity labels, you must **publish them via sensitivity label policies** so that:
- ✅ Users can see and apply labels  
- ✅ Services can enforce protection  
- ✅ Policies apply consistent behaviour across the organisation  

👉 Key difference:
- **Sensitivity labels** → Define classification/protection  
- **Label policies** → Control *who gets those labels and how they are used*  

---

# 🧩 1. What Sensitivity Label Policies Do

A label policy allows you to:

### ✅ 1. Publish Labels
- Assign labels to:
  - Users  
  - Groups (security groups, M365 groups, distribution lists)  

---

### ✅ 2. Control Visibility
- Only assigned users:
  - ✅ See labels in Office apps  
  - ✅ Can apply them  

---

### ✅ 3. Apply Default Labels
- Automatically label:
  - New documents  
  - Unlabeled emails  

---

### ✅ 4. Enforce Behaviour
- Require:
  - Label selection  
- Restrict:
  - Label changes  
- Guide:
  - User decisions via help links  

---

# ⚙️ 2. Key Policy Settings

---

## 🔖 Default Label

### What It Does:
- Applies automatically to:
  - New files  
  - Unlabeled emails  

---

### Benefits:
- ✅ Provides baseline protection  
- ✅ Ensures content is not left unclassified  

---

### ⚠️ Important:
- Avoid using:
  - **Encryption-based labels as default**  
- Why:
  - May block external collaboration  

---

### Example:
- Default label = **General**
- Users can upgrade to:
  - Confidential / Highly Confidential  

---

## 🔐 Require Justification (Label Downgrade Control)

### When Triggered:
- User:
  - Removes a label  
  - Downgrades label (e.g., Confidential → Public)  

---

### Result:
- User must:
  - Provide **justification**  
- Admins can:
  - Review in Activity Explorer  

---

## ✅ Mandatory Labeling

### Ensures:
- Users must apply a label before:
  - Saving a document  
  - Sending email  

---

### Applies To:

#### Documents & Emails:
- Manual  
- Auto-labeling  
- Default label  

---

#### Containers (Teams/Sites):
- Must assign label:
  - At creation  

---

### Benefit:
- ✅ Eliminates unlabeled data  

---

## 🔗 Help Link (User Guidance)

### Purpose:
- Provide:
  - Guidance on label usage  

---

### Appears:
- In Office apps:
  - As “Learn More” link  

---

### Example:
- Link to:
  - Company data classification policy  

---

# 🧭 3. Label Policy Scope

Policy includes:
- Labels included in policy  
- Users/groups assigned  
- Settings (default, mandatory, etc.)  

---

# 🔢 4. Label Policy Priority (Very Important)

### Rule:
- Policies are ordered:
  - Top → Lowest priority  
  - Bottom → Highest priority  

---

### Why This Matters:

If a user belongs to **multiple policies**:
- ✅ All labels are available  
- ⚠️ Conflicting settings → highest priority policy wins  

---

### Example:
- Policy A:
  - Default label = General  
- Policy B (higher priority):
  - Default label = Confidential  

👉 Result:
- Confidential is applied  

---

### Troubleshooting Tip:
If behavior is unexpected:
- ✅ Check policy order  
- ✅ Adjust priority (Move up/down)  

---

# 🧩 5. Multiple Policies Per User

### Allowed:
- Users can have:
  - Multiple label policies  

---

### Behavior:
- ✅ Labels = combined from all policies  
- ✅ Settings = resolved by priority  

---

# 📊 6. Label Limits & Design Guidance

---

## Limits:
- Unlimited labels (with exception):
  - 🔒 Max **500 labels with encryption**

---

## Best Practice:
- Keep labels simple:
  - ✅ 3–5 main labels  
  - ✅ Max 5 sublabels per label  

---

### Why:
- Too many labels:
  - ❌ Confuses users  
  - ❌ Reduces adoption  
  - ❌ Decreases effectiveness  

---

# ⏱️ 7. Deployment Timing

- Policy changes:
  - ✅ Visible within ~24 hours  

---

# ✅ Example Scenario:

### Goal:
Ensure all employees classify documents

---

### Policy Setup:
- Labels:
  - Public  
  - General  
  - Confidential  
- Settings:
  - Default = General  
  - Mandatory labeling = ON  
  - Justification required for downgrade  

---

### Result:
- Users must label all content  
- Default ensures minimum protection  
- Downgrade tracked for auditing  

---

# ✅ Best Practices:

- ✅ Publish labels gradually  
- ✅ Use default label (non-encrypted)  
- ✅ Enable mandatory labeling where possible  
- ✅ Require justification for downgrades  
- ✅ Keep label structure simple  
- ✅ Monitor Activity Explorer for usage  

---

# 🔑 Key Takeaway:

Sensitivity label policies are the **delivery mechanism** for labels—they:

- Control **who sees labels**  
- Enforce **how labels are used**  
- Apply **defaults and restrictions**  
- Resolve **policy conflicts via priority**  

➡️ Together with sensitivity labels, they provide **effective, controlled, and scalable data protection across Microsoft 365**
