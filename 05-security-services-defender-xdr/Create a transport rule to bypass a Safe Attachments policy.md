# Microsoft Defender for Office 365 – Create a Transport Rule to Bypass Safe Attachments Summary

## Overview
Organizations may want certain trusted emails to bypass Safe Attachments scanning to avoid delivery delays.

Common trusted sources include:
- Internal senders
- Trusted scanners
- Fax systems
- Smart hosts

If attachments are considered safe from these trusted sources, administrators can create a transport rule (mail flow rule) to bypass Safe Attachments scanning.

---

# Purpose of the Transport Rule
The transport rule:
- Skips Safe Attachments scanning
- Allows messages and attachments to flow without delay
- Improves delivery speed for trusted mail sources

---

# Where to Configure the Rule

## Navigation Path

1. Microsoft 365 Admin Center
2. Show All
3. Admin Centers → Exchange
4. Exchange Admin Center (EAC)
5. Mail Flow
6. Rules
7. + Add a Rule
8. Create a New Rule

---

# Steps to Create the Bypass Rule

## 1. Name the Rule
- Enter a descriptive rule name

Example:
- Bypass Safe Attachments for Internal Senders

---

# Configure Rule Conditions

## Apply This Rule If

### Example Condition
- The sender
- Is external/internal
- Inside the organization

This allows internal emails to bypass Safe Attachments scanning.

---

# Other Possible Conditions
You can also filter by:
- Specific senders
- Recipients
- Distribution groups
- Attachment types
- Other mail flow properties

---

# Configure the Action

## Do the Following

### Action Selection
1. Modify the message properties
2. Set a message header

---

# Required Message Header

## Header Name
```text
X-MS-Exchange-Organization-SkipSafeAttachmentProcessing

This header tells Microsoft 365 to bypass Safe Attachments scanning.

Header Value
Any value is acceptable
Even a single space works

Important:

Microsoft does NOT use the value itself.
The header only needs a value because the rule requires one.
Save the Rule
Select Save to activate the transport rule.
Knowledge Check Answer

Question:
What should Contoso do if:

Trusted sources should bypass Safe Attachments scanning
Internal emails should not be delayed?

Correct Answer:

Create a transport rule that bypasses Safe Attachments scanning
Key Takeaways
Transport rules can bypass Safe Attachments scanning for trusted mail sources.
Common use cases include internal senders, scanners, and smart hosts.
The rule works by setting a special Exchange message header.
This helps reduce delivery delays for trusted attachments.
The critical header used is:
X-MS-Exchange-Organization-SkipSafeAttachmentProcessing
