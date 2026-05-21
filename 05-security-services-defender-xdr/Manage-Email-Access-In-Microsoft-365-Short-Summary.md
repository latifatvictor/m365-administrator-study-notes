# Manage Email Access in Microsoft 365 - Short Summary

Microsoft 365 manages email security using:
- Exchange Online
- Microsoft Defender for Office 365

These services help organizations:
- Restrict email access
- Block malicious senders
- Prevent phishing
- Stop spam and malware
- Protect compromised accounts

---

# Restrict vs Block Email Access

## Restrict Email Access
Limits who users can:
- Send email to
- Receive email from

Configured using:
- Exchange mail flow rules
- Exchange Online PowerShell

Useful for:
- Preventing compromised users from sending spam
- Protecting sensitive mailboxes
- Limiting communication with external domains

---

# Block Email Access

Completely blocks:
- Domains
- Email addresses
- Senders

Configured using:
- Tenant Allow/Block List
- Microsoft Defender portal

Useful for:
- Blocking phishing domains
- Stopping malicious senders
- Preventing spam delivery

---

# Tenant Allow/Block List

The Tenant Allow/Block List allows admins to:
- Allow trusted senders
- Block malicious senders
- Override spam filtering verdicts

Supports:
- Domains
- Email addresses
- URLs
- Files
- Spoofed senders

---

# Important Security Behavior

## Block Entries
- Take precedence over allow entries
- Can block inbound and outbound communication

## Allow Entries
- Should be used carefully
- Excessive allow entries reduce security

---

# Restricted Users

If a user exceeds outbound sending limits:
- Microsoft adds them to Restricted Users list
- User cannot send email
- User can still receive email

Common causes:
- Compromised account
- Spam activity
- Malware infection

---

# Unblocking Users

Admins can unblock users:
- In Microsoft Defender portal
- Using Exchange Online PowerShell

Recommended actions before unblocking:
- Reset password
- Enable MFA
- Investigate account compromise

---

# Common PowerShell Commands

## View Blocked Users
```powershell
Get-BlockedSenderAddress
