# Microsoft 365 Backup (Preview)

---

# 📌 What is Microsoft 365 Backup?

Microsoft 365 Backup is a Microsoft cloud-native backup and restore solution designed to provide:

- Business continuity
- Disaster recovery
- Fast backup
- Fast restoration
- Ransomware recovery
- Protection against accidental deletion

It is:
- Pay-as-you-go
- Consumption-based
- Integrated into Microsoft 365

---

# 🌍 Availability

Microsoft 365 Backup is available in:

- All worldwide commercial cloud environments

---

# 🎯 Main Purpose

The key focus is not only backup but:

✅ Fast restoration of Microsoft 365 data

This helps organizations recover quickly from:
- Ransomware attacks
- Malicious deletions
- Accidental overwrites
- Data corruption
- Business continuity events

---

# 📦 Protected Workloads

Microsoft 365 Backup protects:

- Exchange Online mailboxes
- SharePoint Online sites
- OneDrive accounts

---

# ⚡ Key Benefits

## Fast Backup
- Backup created within hours

---

## Fast Restore
- Restore operations complete within hours

---

## SharePoint & OneDrive Full Fidelity Restore
Restores:
- Entire site/account
- Exact prior state
- Point-in-time rollback

---

## Granular Restore Support
Future support includes:
- File-level restore
- Granular recovery

---

## Exchange Mailbox Restore
Supports:
- Full mailbox restore
- Granular item restore
- Search-based restore

---

## Security & Compliance Integration
Backup stays within Microsoft security boundary.

---

# 🤝 Microsoft & Partner Solutions

Microsoft 365 Backup can be used:

## Directly Through:
- Microsoft 365 Admin Center

OR

## Through Partner Applications
(ISVs integrated with Microsoft 365 Backup Storage)

---

# 📌 Partner Solution Benefits

Partner solutions may provide:
- Single backup dashboard
- Multi-platform backup
- Enhanced workflows
- Centralised management

---

# 💰 Pricing Model

Microsoft 365 Backup uses:

- Pay-as-you-go pricing

Current list price:
- $0.15 per GB/month

---

# 📊 What Determines Cost?

Backup pricing is based on:

## Exchange
- Mailbox size
- Online archives
- Deleted items

---

## SharePoint
- Live SharePoint site size

---

## OneDrive
- Live OneDrive account size

---

## Recycle Bin Data
Includes:
- First-stage recycle bin
- Second-stage recycle bin

---

# ⚠️ Important Pricing Notes

Microsoft does NOT charge for:
- Restore points
- Restore operations
- Azure storage APIs

---

# 📅 Retention Billing Logic

Backup retention:
- 365 days

Even deleted data is billed until:
- Backup retention expires

---

# 💡 Example

If a SharePoint site:

Month 1:
- Size = 1 GB

Month 2:
- User deletes 0.5 GB

Billing still remains:
- 1 GB

Reason:
- Deleted data retained for backup purposes

After 1 year:
- Deleted backup expires
- Billing reduces accordingly

---

# 🧮 Pricing Calculator

Microsoft provides:
- Microsoft 365 Backup Pricing Calculator

Purpose:
- Estimate future backup consumption and cost

---

# 📌 Pricing Calculator Uses

The calculator estimates:
- Storage growth
- Monthly changes
- Backup expansion
- Future costs

---

# 📈 Forecasting Factors

The calculator considers:
- Data growth trends
- Deleted content trends
- New mailboxes/sites/users
- Historical storage usage

---

# 🏗️ Microsoft 365 Backup Architecture

---

# 🔒 Key Security Features

## Data Residency Protection
Data never leaves:
- Microsoft 365 trust boundary
- Geographic residency location

---

## Immutable Backups
Backups:
- Cannot be modified
- Protected against overwrite
- Only removable during offboarding

---

## Physically Redundant Storage
Microsoft stores:
- Multiple redundant copies
- Across geographically separate datacentres

---

# 🛡️ Protection Against Ransomware

Microsoft uses:
- Append-only storage

Meaning:
- Old blobs cannot be modified
- Historical data protected
- Backup integrity preserved

---

# 📌 Exchange Backup Protection

Exchange items:
- Stored immutably
- Cannot be modified by Outlook/OWA/MFCMAPI

This protects against:
- Corruption
- Malicious overwrite attempts

---

# ⚡ Backup Policy Performance

When a backup policy is created:

## Average Processing Time
- Up to 60 minutes to process
- Additional 60 minutes to create restore points

---

# 📌 Important Note

Restore points are physically created immediately after activation, even if visibility takes longer.

---

# ⚡ Restore Performance

Restore speed depends on:

- Restore type
- Restore location
- Restore point selected

---

# 🚀 Fastest Restore Method

Fastest option:
- In-place restore
- Same URL restore
- Recommended faster restore point

---

# 📊 Restore Performance Expectations

## Example Performance

Scenario:
- 1,000 protection units
- Average 30 GB each

Expected restore completion:
- Less than 12 hours

---

# 📌 Protection Unit Definition

A protection unit is:
- One SharePoint site
- One OneDrive account
- One Exchange mailbox

---

# 🔄 Types of Restore

## SharePoint & OneDrive
Supports:
- Full site restore
- Full account restore
- Same URL restore
- New URL restore

---

## Exchange
Supports:
- Mailbox restore
- Item-level restore
- Search-based restore

---

# 💼 Real Work Examples

---

# Scenario 1: Ransomware Attack

A ransomware attack encrypts SharePoint files.

Solution:
- Restore SharePoint site to earlier restore point

Result:
- Business restored quickly

---

# Scenario 2: Accidental File Deletion

User deletes important OneDrive data.

Solution:
- Restore OneDrive account to previous healthy state

---

# Scenario 3: Mailbox Corruption

Executive mailbox accidentally purged.

Solution:
- Restore mailbox items from backup

---

# 🔐 Security Advantages

- Immutable backups
- Microsoft-native protection
- Geographically redundant copies
- Fast disaster recovery
- No external backup movement

---

# ⚠️ Important Limitations

Currently Preview feature:
- Features may change
- Pricing may evolve
- Granular restore still expanding

---

# 🧠 Interview Questions

## Q1: What is Microsoft 365 Backup?
A Microsoft-native backup and restore solution for Exchange, SharePoint, and OneDrive.

---

## Q2: What workloads are protected?
- Exchange Online
- SharePoint Online
- OneDrive

---

## Q3: What is the pricing model?
Pay-as-you-go at approximately $0.15/GB/month.

---

## Q4: Does Microsoft charge for restore operations?
No.

---

## Q5: What is immutable backup?
Backup data cannot be modified or overwritten.

---

## Q6: What is append-only storage?
Storage where new data can be added but existing data cannot be altered.

---

## Q7: What is a protection unit?
A mailbox, SharePoint site, or OneDrive account.

---

# 🔥 Key Exam Points

- Microsoft 365 Backup is consumption-based
- Available globally in commercial clouds
- Protects Exchange, SharePoint, OneDrive
- Uses immutable backup storage
- Data remains within Microsoft trust boundary
- Supports fast restore and rollback
- Restore operations are not billed
- Retention lasts 365 days
- Append-only storage protects against ransomware

---

# 🛠️ Administration & Management

Admins manage Microsoft 365 Backup through:
- Microsoft 365 Admin Center
- Partner applications
- Backup policies
- Restore workflows

---

# 📌 Best Practices

- Protect critical SharePoint sites
- Protect executive mailboxes
- Regularly review restore capability
- Understand retention billing
- Use same URL restore for fastest recovery
- Monitor backup policy status
- Test recovery procedures periodically

---

# 🚀 Summary

Microsoft 365 Backup provides:
- Fast cloud-native backup
- Business continuity
- Disaster recovery
- Ransomware resilience
- Immutable storage protection
- Rapid restoration

It is designed for:
- Enterprise resilience
- Microsoft 365 protection
- Fast operational recovery
- Reduced downtime

---
