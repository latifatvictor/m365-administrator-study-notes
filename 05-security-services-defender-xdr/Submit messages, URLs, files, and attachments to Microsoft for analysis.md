# Microsoft Defender for Office 365 – Submissions Summary

## Overview
Microsoft 365 organizations with Exchange Online mailboxes can submit:
- Emails
- URLs
- Attachments
- Files
- Teams messages

to Microsoft for security analysis using the **Submissions** page in the Microsoft Defender portal.

Purpose:
- Improve Microsoft threat detections
- Reduce investigation and remediation effort
- Improve organizational productivity and security posture

---

# Why Submissions Are Important

## 1. Manage False Positives and False Negatives
- False Positive = Legitimate message marked as malicious
- False Negative = Malicious message allowed through

Submitting these helps Microsoft improve detection accuracy.

---

## 2. Increase Attack Visibility
- Users can report suspicious threats targeting the organization.
- Gives administrators better visibility into phishing and malware campaigns.

---

## 3. Block Suspicious Entities
Organizations can quickly protect users by blocking:
- Malicious URLs
- Attachments
- Email senders
- Domains

---

## 4. Optimize Security Operations
- Reduces need for manual triage of SecOps mailboxes
- Centralizes investigation and response within Microsoft Defender portal

---

## 5. Increase Productivity
Benefits include:
- Quick reporting through Outlook Report Message add-ins
- Admin ability to review and notify users
- Centralized investigations
- Automated investigations (requires Defender for Office 365 Plan 2)

---

# Automated Investigations (Plan 2)
With Microsoft Defender for Office 365 Plan 2:
- Automated investigations can:
  - Hunt threats
  - Confirm malicious campaigns
  - Trigger remediation automatically
- Provides near 24/7 threat coverage

---

# Submissions Page in Microsoft Defender Portal

Path:
- Actions & Submissions → Submissions

Tabs available:
- Emails
- Teams messages
- Email attachments
- URLs
- Files
- User-reported messages

---

# Checks Microsoft Performs During Analysis

## Email Authentication
- Verifies whether authentication passed or failed

## Policy Hits
- Reviews policies or overrides that allowed or blocked messages

## Payload Reputation / Detonation
- Analyzes URLs and attachments for malicious activity

## Grader Analysis
- Human review to confirm if content is malicious

---

# Important Government Cloud Limitation
For:
- GCC
- GCC High
- DoD

Only these checks occur:
- Email authentication
- Policy hits

The following are NOT performed:
- Payload detonation
- Reputation analysis
- Human grader analysis

Reason:
- Compliance and data boundary restrictions

---

# User vs Admin Submissions

## User-Reported Messages
Users can report via:
- Report Message add-in
- Report Phishing add-in
- Outlook Web Report button

Admins can:
- Review submissions
- Classify as phishing/spam/safe
- Track phishing simulations separately

---

## Admin-Reported Messages
Admins can submit from:
- Submissions
- Explore
- Advanced Hunting
- Alerts
- Quarantine
- Email

Admins can submit:
- Emails
- Attachments
- URLs
- Files

---

# Defender for Endpoint Integration
Organizations with:
- Microsoft Defender XDR
OR
- Defender for Endpoint Plan 2

can submit files through the Files tab.

---

# Submission Limits

## Time Restrictions
Emails can be submitted if:
- Less than 30 days old
- Still available in mailbox

## Throttling Limits
- 150 submissions per 15 minutes
- Same submission:
  - Max 3 times in 24 hours
  - Max once every 15 minutes

---

# Tracking Submission Results

After analysis:
- Submission status changes to Completed
- Admins can review:
  - Original item
  - Status
  - Microsoft verdict
  - Analysis results

Admins can also:
- Mark verdicts
- Notify users

---

# Tenant Allow/Block List Integration

When admins submit false positives:
- Allow entries may automatically be created.

Possible locations:
- Domains & email addresses
- URLs
- Files
- Spoofed senders

---

# URL False Positive Behaviour
If a URL is incorrectly blocked:
- Microsoft allows future URL variations automatically.

Example:
- Reporting:
  - www.contoso.com/abc

also allows:
- www.contoso.com/abc?id=1
- www.contoso.com/abc/xyz

No need to report every variation separately.

---

# Email False Positive Handling

## Spoof Intelligence Blocks
- Sender added to Spoofed Senders allow list

## Anti-Phishing Impersonation Blocks
- Sender/domain added to Trusted Senders and Domains

## File-Based Filtering
- File added to Files allow list

## URL-Based Filtering
- URL added to URL allow list

## Other Filtering Reasons
- Sender/domain added to Domains & Addresses allow list

---

# Key Takeaways
- Submissions improve Microsoft threat intelligence and organizational protection.
- Users and admins both play important roles in reporting threats.
- Defender for Office 365 Plan 2 adds powerful automated investigation capabilities.
- False positive reporting automatically improves future mail flow handling.
- Tenant Allow/Block Lists are dynamically updated based on submission results.
