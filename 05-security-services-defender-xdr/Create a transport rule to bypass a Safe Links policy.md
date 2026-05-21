# Microsoft Defender for Office 365 – Bypass Safe Links Quick Notes

## Purpose
Create a transport (mail flow) rule to bypass Safe Links scanning for trusted senders or internal mail.

---

# Navigation Path
1. Microsoft 365 Admin Center
2. Show All
3. Admin Centers → Exchange
4. Exchange Admin Center (EAC)
5. Mail Flow
6. Rules
7. + Add a Rule
8. Create a New Rule

---

# Configure Rule

## Apply This Rule If
Example:
- The sender
- Is external/internal
- Inside the organization

Other possible conditions:
- Specific senders
- Recipients
- Distribution groups
- Attachment types

---

# Action Configuration

## Do The Following
1. Modify the message properties
2. Set a message header

---

# Required Header

```text
X-MS-Exchange-Organization-SkipSafeLinksProcessing

Purpose:

Bypasses Safe Links scanning
Header Value
Any value works
Even a single space

Important:

Microsoft does NOT use the value itself.
Final Step
Save the transport rule
Key Exam Points
Safe Links can be bypassed using a transport rule.
Transport rules are configured in Exchange Admin Center.
The required bypass header is:
X-MS-Exchange-Organization-SkipSafeLinksProcessing
Common use case:
Trusted internal senders or systems
