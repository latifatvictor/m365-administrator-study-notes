## Configure Email Notifications for DLP Policies – Summary

### Overview:
Email notifications and policy tips in Microsoft Purview DLP help organizations:
- ✅ Inform users of policy violations  
- ✅ Encourage compliant behavior  
- ✅ Reduce unnecessary blocking  
- ✅ Educate users while maintaining productivity  

---

## Why Use Notifications:
- Helps users understand **why an action is risky**
- Enables **self-correction**
- Supports **compliance training in real time**
- Reduces reliance on strict blocking  

---

## Types of User Notifications:

---

### 1. Email Notifications
- Sent when a DLP policy rule is triggered  
- Inform:
  - Users  
  - Content owners  
  - Administrators  

---

### 2. Policy Tips
Displayed in real-time across:

- Outlook (email composition)
- SharePoint / OneDrive (file view)
- Office apps (Word, Excel, PowerPoint)

✅ Provide immediate warning before or during action  

---

## Where Policy Tips Appear:

| Location | Behavior |
|---------|---------|
| Outlook | Banner above email while composing |
| SharePoint / OneDrive | Warning icon + details pane |
| Office Apps | Message bar + File → Info view |

---

## How to Configure Notifications:

---

### Step 1: Enable Notifications in Rule
- During policy creation:
  - Go to **Define policy settings**
  - Select **Create or customize advanced DLP rules**

---

### Step 2: Create/Edit Rule
- Click **+ Create rule**
- Enter rule name  

---

### Step 3: Enable User Notifications
- Turn **User notifications = On**

---

### Step 4: Configure Notification Options:

#### Endpoint Devices:
- ✅ Show policy tip when activity is restricted  

---

#### Microsoft 365 Services:
- ✅ Notify users with policy tips  

---

### Step 5: Save Rule
- Apply other rule settings  
- Save changes  

---

## Email Notification Configuration Options:

---

### Who Gets Notified:
You can send notifications to:
- Content owner  
- Last modifier  
- Site owner  
- Specific user  

⚠️ Limitation:
- Only **individual users** (no groups/distribution lists)

---

### When Notifications Are Sent:
- ✅ Only triggered for **new content/actions**
- ❌ Editing existing files → policy tip only (no email)

---

### Internal vs External:
- ✅ Notifications sent only to **internal users**
- ❌ External users do NOT receive notifications  

---

## Default Email Notifications:

### Subject Examples:
- "Notification"  
- "Message Blocked" (email)  
- "Access Blocked" (documents)  

---

### Behavior:

#### For Documents:
- Includes:
  - Link to file  
  - Option to resolve issue  

---

#### For Emails:
- Includes:
  - Copy of blocked email as attachment  

---

### Default Messages (Examples):

| Scenario | Message |
|----------|--------|
| Notification only | Item conflicts with policy |
| Block + allow override | Warning + possible block |
| Block (no override) | Access completely blocked |

---

## Custom Email Notifications:

### Features:
- ✅ HTML supported  
- ✅ Rich formatting (branding, images)  
- ✅ Max length: 5,000 characters  

---

### Useful Tokens:

| Token | Purpose |
|------|--------|
| %%AppliedActions%% | Shows actions taken |
| %%ContentURL%% | Link to content |
| %%MatchedConditions%% | Explains why triggered |

---

### Example (Concept):
```html
Alert: Sensitive data detected  
Action: %%AppliedActions%%  
Location: %%ContentURL%%  
Reason: %%MatchedConditions%%
