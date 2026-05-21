## Configure Policy Tips for DLP Policies – Summary

### Overview:
Policy tips in Microsoft Purview DLP provide **real-time notifications to users** when they interact with sensitive data. They help:
- ✅ Raise awareness  
- ✅ Prevent accidental data leaks  
- ✅ Guide users to compliant behavior  
- ✅ Allow controlled overrides (when appropriate)  

---

## What Policy Tips Can Do:

### 1. Notify Users
- Warn users when content:
  - Contains sensitive data  
  - Violates a DLP policy  

---

### 2. Allow Overrides
Depending on configuration, users can:
- ✅ Override the policy  
- ✅ Provide business justification  
- ✅ Report false positives  

---

### 3. Log User Actions
- Overrides and false positives are:
  - ✅ Recorded  
  - ✅ Available in DLP reports  

---

## Example Policy Tip Scenario:

### Rules:
- **Rule 1 (Low Risk)**:
  - < 5 sensitive items  
  - Internal sharing  
  - ✅ Notify only  

---

- **Rule 2 (Medium Risk)**:
  - > 5 sensitive items  
  - Internal sharing  
  - ❗ Block + allow override with justification  

---

- **Rule 3 (High Risk)**:
  - > 5 sensitive items  
  - External sharing  
  - 🚫 Block with NO override  

---

## Override Behavior:

### Important Rules:
- Override applies **per rule**
- Cannot override:
  - ❌ Notification action itself  
- Only shown when:
  - Block action is enabled  

---

### Priority Logic:
- If multiple rules match:
  - ✅ Only **most restrictive rule tip is shown**  

---

## Override Options Matrix:

| Rule Type | Override Allowed | Justification Required |
|----------|-----------------|-----------------------|
| Notify only | ❌ No | ❌ No |
| Notify + Block | ❌ No | ❌ No |
| Notify + Block + Override | ✅ Yes | Optional |
| Notify + Block + Override + Justification | ✅ Yes | ✅ Yes |
| Notify + Block + Override + False positive | ✅ Yes | Optional |

---

## Policy Tips in SharePoint & OneDrive:

### Indicators:
- ⚠️ Warning icon → Notification  
- 🚫 Block icon → Access restricted  

---

### User Actions:
1. Select file  
2. Open **Info pane**  
3. View policy tip  
4. Choose:
   - Resolve  
   - Override  
   - Report false positive  

---

### Notes:
- Tips may take time to appear  
- Icons disappear after resolution  

---

## Policy Tips in Outlook:

### Where They Appear:
- At top of email while composing  

---

### Triggered By:
- Sensitive data in:
  - Email body  
  - Subject  
  - Attachments  

---

### User Options:
- View details  
- Override (if allowed)  
- Provide justification  

---

### Limitations:
- ❌ No tips when:
  - Message is encrypted  
  - Encryption detection is used  

---

## Policy Tips in Office Apps (Word, Excel, PowerPoint):

### Display Locations:
- Message bar  
- File → Info view  

---

### User Actions:
- Ignore  
- Override  
- Report false positive  

---

### Special Behavior:
- Users can disable tips:
  - Notification tips → hidden  
  - Blocking/override tips → still shown  

---

## Customizing Policy Tips:

### Characteristics:
- Plain text only  
- Max 256 characters  
- No HTML or tokens  

---

### Example:
> “This file contains sensitive data. Please remove or justify before sharing externally.”

---

## Default Messages:

### Examples:
- “This item conflicts with a policy in your organization.”  
- “This file may be blocked if not resolved.”  
- “Access is restricted due to policy violation.”  

---

## Key Considerations:

### Deployment:
- Policy tips appear with slight delay  
- Synced asynchronously  

---

### System Behavior:
- Only one policy tip shown (highest priority)  
- Applies across:
  - Teams  
  - Exchange  
  - SharePoint  
  - OneDrive  
  - Office apps  

---

### Compatibility:
- Policy tips work from:
  - Purview OR Exchange  
- Not both simultaneously  

---

## Best Practices:
- ✅ Use clear, simple language  
- ✅ Align tips with company policy  
- ✅ Enable justification for medium-risk scenarios  
- ✅ Avoid override for high-risk scenarios  
- ✅ Use tips for training users  

---

## Key Takeaway:
Policy tips are a **critical user-facing component** of DLP that:
- Guide users in real time  
- Prevent risky actions before they happen  
- Balance security with productivity  

➡️ When configured properly, policy tips transform DLP from a **blocking system into an intelligent user guidance tool**
