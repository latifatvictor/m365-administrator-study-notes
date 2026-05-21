# Microsoft Defender for Office 365 – Modify Existing Safe Attachments Policy Summary

## Overview
Administrators can modify existing Safe Attachments policies through the Microsoft Defender portal.

The settings available during modification are the same settings used when creating a Safe Attachments policy.

---

# Steps to Modify a Safe Attachments Policy

## Navigation Path

1. Open Microsoft 365 Admin Center
2. Select:
   - Show All
3. Under Admin Centers:
   - Select Security
4. In Microsoft Defender Portal:
   - Select Policies & Rules
5. Select:
   - Threat Policies
6. Under Policies:
   - Select Safe Attachments
7. Select the required policy
   - Click the policy itself
   - Do NOT select the checkbox
8. Edit required settings in the policy details pane

---

# Editable Settings
The editable settings are identical to those available during policy creation, including:
- Safe Attachments response actions
- Recipient filters
- Quarantine policies
- Redirect settings
- Exceptions
- Enable/disable settings

---

# Safe Attachments Policy Priority

## Automatic Priority Assignment
Safe Attachments automatically assigns priorities based on creation order.

Example:
- First policy created = Priority 0
- Second policy created = Priority 1
- Third policy created = Priority 2

---

# Priority Rules

## Lower Number = Higher Priority
- Priority 0 = Highest priority
- Higher numbers = Lower priority

---

# Policy Processing Behaviour

Safe Attachments processes policies:
- In priority order
- Highest priority first

Example:
1. Priority 0
2. Priority 1
3. Priority 2
4. Priority 3

---

# Important Processing Rule

## Processing Stops After First Match
Once a policy applies to a recipient:
- No further policies are evaluated.

---

# Priority Restrictions

## Duplicate Priorities
- Two policies CANNOT share the same priority value.

---

# Microsoft Defender XDR vs PowerShell

## Microsoft Defender XDR
- Priority can ONLY be changed AFTER policy creation.

---

## Exchange PowerShell
- Priority can be assigned DURING rule creation.
- Changing priorities may automatically adjust other rule priorities.

---

# Key Takeaways
- Existing Safe Attachments policies can be modified from Microsoft Defender portal.
- Policies are processed according to priority.
- Lower numerical value means higher priority.
- Priority 0 is always the highest priority.
- Safe Attachments stops processing after the first matching policy.
- Microsoft Defender XDR allows priority changes only after creation, while PowerShell allows priority assignment during creation.
