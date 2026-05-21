## Retention Policies & Retention Labels – Microsoft Purview Summary

### Overview:
- Help organizations **manage, retain, and delete data** for:
  - Compliance (legal/regulatory)
  - Risk reduction
  - Data governance
- Apply to:
  - Emails, documents, chats, files, etc.

---

## Core Retention Actions:
- **Retain-only** → Keep content indefinitely or for a set period  
- **Delete-only** → Automatically delete after a period  
- **Retain + Delete** → Keep, then permanently delete (most common)  

---

## How Retention Works (In Place):
- Content stays **in its original location**
- Users can continue working normally
- If content is changed or deleted:
  - A **copy is preserved** in secure storage

### Storage Locations:
- SharePoint/OneDrive → **Preservation Hold Library**  
- Exchange → **Recoverable Items folder**  
- Teams/Yammer → **SubstrateHolds (hidden folder)**  

---

## Retention Policies:

### Purpose:
- Apply retention rules at the **container level**

### Scope:
- Entire organization OR specific:
  - Mailboxes
  - SharePoint sites
  - OneDrive accounts
  - Teams, Yammer, etc.

### Characteristics:
- Easy bulk application  
- Items inherit settings  
- Retention based on:
  - Created date
  - Last modified date (files only)  

⚠️ Limitation:
- Retention settings **don’t travel** if content is moved  

---

## Retention Labels:

### Purpose:
- Apply retention at the **item level** (file, email, document)

### Key Features:
- Travel with content **within Microsoft 365**
- Flexible retention start triggers:
  - Created date
  - Last modified date
  - When labeled
  - Event-based (e.g., contract end)

---

### Advanced Capabilities:
- Auto-label using:
  - Sensitive data types  
  - Keywords  
  - Trainable classifiers  
- Manual labeling by users  
- Default labels for locations  
- End-of-retention actions:
  - Delete content  
  - Apply new label  
  - Require disposition review  

---

### Records Management:
- Labels can:
  - Mark content as **records**
  - Prevent editing or deletion

---

## Retention Policies vs Retention Labels:

| Feature | Retention Policies | Retention Labels |
|--------|------------------|------------------|
| Level | Container (site/mailbox) | Item (file/email) |
| Flexibility | Low | High |
| Travels with content | ❌ | ✅ (within M365) |
| Automated classification | Limited | Advanced |
| Records management | ❌ | ✅ |

---

## Label Application Methods:
- Manual (users/admins)
- Auto-apply policies
- Default labels (SharePoint/Outlook)
- Outlook rules
- AI (classifiers)

✅ Only **one retention label per item**

---

## Special Use Cases for Labels:
- Legal documents (retain longer)
- Expiring contracts (event-based retention)
- Confidential records (locked as records)
- Content classification (label only, no action)

---

## DLP Integration:
- Retention labels can be used as **conditions in DLP policies**
- Example:
  - Block sharing of labeled confidential documents

---

## Policy Lookup:
- Check applied policies via **Policy Lookup tool**
- Search using:
  - User email  
  - Site URL  
  - Microsoft 365 group  

---

## Key Benefits:
- ✅ Automated compliance enforcement  
- ✅ Reduced storage and risk  
- ✅ Flexible retention strategies  
- ✅ Improved governance and visibility  
- ✅ Seamless user experience  

---

## Key Takeaway:
Retention policies and retention labels enable organizations to **efficiently govern data lifecycle**, ensuring that data is **retained when needed and securely deleted when no longer required**, while maintaining compliance and minimizing risk.
