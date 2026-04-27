# Examine Groups in Microsoft 365

---

## 🔑 Overview

Groups in Microsoft 365 are used to manage users collectively for:

- permissions
- collaboration
- communication
- security policies

Instead of managing users individually, admins assign access and policies to groups.

---

## 🧠 Why Groups Matter

Groups help organisations:

- simplify access management
- assign permissions to multiple users at once
- enable collaboration (Teams, SharePoint, Outlook)
- enforce security (Conditional Access, device policies)

---

## 📊 Types of Groups in Microsoft 365

### 1. Microsoft 365 Group (Recommended)

- Includes:
  - shared mailbox
  - calendar
  - SharePoint site
  - Teams (if enabled)
  - Planner
- Best for collaboration

👉 Use when:
You want a full collaboration workspace for a team

---

### 2. Distribution Group

- Email-only group
- Sends messages to all members

👉 Use when:
You only need to send emails to a group

---

### 3. Mail-enabled Security Group

- Combines:
  - email distribution
  - permission assignment

👉 Use when:
You need both email and access control

⚠️ Limitation:
- No dynamic membership
- Cannot contain devices

---

### 4. Security Group

- Used for access control only
- No email functionality

👉 Use when:
You only need to assign permissions

Examples:
- SharePoint access
- OneDrive access
- Conditional Access policies

---

### 5. Dynamic Distribution Group

- Membership updates automatically
- Based on rules like:
  - department
  - job title
  - location

👉 Use when:
You want automated email distribution lists

⚠️ Managed in:
Exchange Online (PowerShell or admin center)

---

### 6. Shared Mailbox

- Shared email account
- Multiple users can:
  - read emails
  - reply as the mailbox

👉 Use when:
Multiple people manage one inbox

Examples:
- support@company.com
- info@company.com

---

## 🏗️ Microsoft 365 Group Components

A Microsoft 365 group automatically creates:

- Outlook shared inbox
- shared calendar
- SharePoint site
- document library
- Planner
- Power BI workspace
- OneNote notebook
- Teams (if created from Teams)

---

## 🔗 Microsoft 365 Groups and Teams

- Every Team = Microsoft 365 Group in the background
- Group manages membership
- Team provides collaboration interface

👉 Important:

- Adding/removing users in Teams updates the group
- Removing users removes access to:
  - Teams
  - SharePoint
  - Planner
  - other connected services

---

## ⏱️ Membership Sync Behaviour

| Action | Effect |
|---|---|
| Remove user from group | Immediate removal from SharePoint & resources |
| Remove user from Teams | Removes from group |
| Changes outside Teams | Can take up to 24 hours to sync |
| Chat access removal | Can take up to 2 hours |

👉 Best practice:
Always manage users from Teams when dealing with Teams-based groups

---

## 🗑️ Deleting Groups and Teams

When a Microsoft 365 Group is deleted:

- Outlook mailbox is removed
- SharePoint site is marked for deletion
- Teams is removed
- Planner data is deleted

⏱️ Timing:

- Team disappears immediately
- Outlook updates ~20 minutes
- SharePoint deletion follows

---

## ⚙️ Where to Create Groups

| Group Type | Where to Create |
|---|---|
| Microsoft 365 Group | Admin Center, Outlook, Teams, SharePoint |
| Distribution Group | Admin Center, Exchange Admin Center |
| Mail-enabled Security Group | Admin Center, Exchange Admin Center |
| Security Group | Admin Center, Entra Admin Center |
| Dynamic Distribution Group | Exchange Admin Center |
| Shared Mailbox | Admin Center |

---

## 💼 Real-Life IT Scenarios

- Creating Teams for departments
- Setting up distribution lists for announcements
- Assigning SharePoint permissions using security groups
- Creating dynamic groups for HR or departments
- Managing shared mailboxes for support teams

---

## ⚠️ Common Mistakes

- Using distribution groups for collaboration (use M365 group instead)
- Assigning permissions directly to users instead of groups
- Managing Teams membership outside Teams
- Forgetting group lifecycle and cleanup
- Using too many group types without governance

---

## 🧠 Best Practices

- Use Microsoft 365 Groups for collaboration
- Use Security Groups for permissions
- Use Dynamic Groups to automate membership
- Apply naming conventions for groups
- Regularly review and clean up unused groups

---

## 🔥 Interview Questions

### Q1: Which group type is best for collaboration?

Microsoft 365 Group

---

### Q2: What is the difference between a security group and a distribution group?

- Security group = permissions
- Distribution group = email only

---

### Q3: What happens when you create a Team?

A Microsoft 365 Group is created in the background

---

### Q4: Can you assign permissions using a distribution group?

No

---

### Q5: Which group updates membership automatically?

Dynamic distribution group

---

## 🧠 Summary

- Groups simplify user management
- Different group types serve different purposes
- Microsoft 365 Groups are best for collaboration
- Security groups are best for permissions
- Teams relies on Microsoft 365 Groups

👉 Choosing the right group type is critical for scalability, security, and organisation.
