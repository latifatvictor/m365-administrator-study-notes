# Microsoft Defender for Office 365 – Creating Safe Attachments Policies Summary

## Overview
Safe Attachments is a feature in Microsoft Defender for Office 365 that:
- Scans inbound email attachments for malware
- Uses a virtual environment (sandboxing) to analyze attachments before delivery
- Works alongside Exchange Online Protection (EOP)

---

# Important Note
There is NO default Safe Attachments policy.

To enable Safe Attachments scanning, administrators must create one or more Safe Attachments policies.

---

# Where Safe Attachments Policies Can Be Configured

## Supported Management Methods
- Microsoft Defender XDR
- Exchange Online PowerShell
- Standalone EOP PowerShell

---

# Safe Attachments Policy Components

A Safe Attachments implementation consists of:

## 1. Safe Attachments Policy
Defines:
- Malware response actions
- Quarantine behaviour
- Redirect settings

## 2. Safe Attachments Rule
Defines:
- Policy priority
- Recipient scope
- Users/groups/domains affected

---

# Important Behaviour in Microsoft Defender XDR

When using Microsoft Defender XDR:

## Creating a Policy
- Creates BOTH:
  - Safe Attachments Rule
  - Safe Attachments Policy
- Both share the same name

## Modifying a Policy
Changes to:
- Name
- Priority
- Enabled/disabled state
- Recipient filters

modify the RULE.

Other settings modify the POLICY.

## Removing a Policy
- Deletes both:
  - Rule
  - Associated policy

---

# Required Administrative Roles

To manage Safe Attachments policies, administrators must belong to:

## Microsoft Defender Portal
- Organization Management
OR
- Security Administrator

## Exchange Online
- Organization Management

---

# Steps to Create a Safe Attachments Policy in Microsoft Defender XDR

## Navigation Path
1. Microsoft 365 Admin Center
2. Show All
3. Admin Centers → Security
4. Microsoft Defender Portal
5. Policies & Rules
6. Threat Policies
7. Safe Attachments
8. Create

---

# Policy Configuration Pages

## 1. Name Your Policy
Configure:
- Policy name
- Optional description

---

## 2. Users and Domains Page

### Supported Recipient Filters

#### Users
Applies to:
- Mailboxes
- Mail users
- Mail contacts

#### Groups
Supports:
- Microsoft 365 Groups
- Distribution Groups
- Mail-enabled Security Groups

Not Supported:
- Dynamic Distribution Groups

#### Domains
Applies to recipients within specified accepted domains.

---

# Exceptions
You can exclude:
- Users
- Groups
- Domains

---

# Logic Behaviour

## Same Condition Type
Uses OR logic.

Example:
- recipient1 OR recipient2

---

## Different Condition Types
Uses AND logic.

Example:
- User must match BOTH:
  - Stacy@contoso.com
  - Executives group

---

# Safe Attachments Response Options

## 1. Off
- Safe Attachments scanning disabled
- EOP malware scanning still active
- Typically used for trusted internal systems

Microsoft generally does NOT recommend this setting.

---

## 2. Monitor
- Delivers message
- Tracks malware activity
- Useful for analysis/testing environments

---

## 3. Block (Recommended Default)
- Blocks messages with malicious attachments
- Quarantines messages
- Only admins can:
  - Review
  - Release
  - Delete

Benefits:
- Prevents repeated attacks
- Automatically blocks future instances

---

## 4. Dynamic Delivery (Preview Feature)
- Delivers email immediately
- Replaces attachment with placeholder during scanning
- Reattaches file if safe

Additional Features:
- Safe preview of PDFs and Office files
- Avoids delivery delays
- Malicious files still quarantined

---

# Quarantine Policy Options

## AdminOnlyAccessPolicy (Default)
- Only admins can manage quarantined messages
- Users receive no notifications

Typically used for:
- High-confidence phishing
- Malware detections

---

## DefaultFullAccessPolicy
- Users can:
  - Review
  - Release
  - Delete quarantined messages
- No notifications sent

---

## DefaultFullAccessWithNotificationPolicy
- Users receive notifications
- Users can manage quarantined messages

Used in:
- Standard preset policies
- Strict preset policies

---

# Redirect Messages Option

## Enable Redirect
- Sends malware-detected messages to a specified mailbox
- Used for:
  - Analysis
  - Investigation

Important:
- Works ONLY with Monitor mode

Microsoft recommends enabling redirection for:
- Standard policies
- Strict policies

---

# Final Steps
1. Review settings
2. Edit if required
3. Submit
4. Select Done

---

# Knowledge Check Answer

Question:
Which Safe Attachments option:
- Delivers messages with attachments
- Tracks what happens with detected malware?

Correct Answer:
- Monitor

---

# Key Takeaways
- Safe Attachments requires manual policy creation.
- Policies determine malware handling behaviour.
- Rules determine who receives protection.
- Block is the recommended default action.
- Dynamic Delivery improves user experience while maintaining security.
- Quarantine policies control user/admin access to quarantined content.
