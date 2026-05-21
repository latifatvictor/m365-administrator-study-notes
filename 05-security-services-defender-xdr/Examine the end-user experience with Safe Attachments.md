# Microsoft Defender for Office 365 – End-User Experience with Safe Attachments Summary

## Overview
The primary goal of Safe Attachments is to protect users from opening malicious or unsafe email attachments.

Administrators can configure different Safe Attachments actions, including:
- Block
- Replace
- Dynamic Delivery

Most organizations prefer Dynamic Delivery because it improves the user experience by reducing email delivery delays.

---

# Block Attachments

## How It Works
When a Safe Attachments policy is configured with:
- Block

the system:
- Prevents delivery of the entire email
- Blocks both:
  - Message body
  - Attachment

---

# End User Experience with Block

Instead of receiving the original email, the user receives:
- A notification message

The notification explains:
- A malicious attachment was detected
- The original email and attachment were blocked

---

# When to Use Block

Best suited for:
- High-risk users
- Highly sensitive environments
- Strict security enforcement scenarios

Use Block when:
- Security is more important than uninterrupted delivery
- Non-delivery of suspicious emails is acceptable

---

# Dynamic Delivery (Recommended)

## Purpose
Dynamic Delivery improves user productivity by:
- Eliminating attachment scanning delays
- Delivering the message body immediately

---

# Why Dynamic Delivery Is Preferred

Traditional sandboxing introduces:
- Scanning latency
- Delivery delays

Dynamic Delivery solves this by:
- Allowing users to access the email immediately
- Scanning attachments in the background

---

# End User Experience with Dynamic Delivery

## Initial Email Delivery
The user receives:
- The original email body
- A placeholder attachment instead of the actual file

The placeholder informs the user:
- The attachment is currently being scanned

---

# What Happens After Scanning?

## If the Attachment Is Safe
Safe Attachments:
- Reattaches the clean file
- Updates the original email in the Inbox

The user can then:
- Open the attachment normally

---

## If the Attachment Is Malicious
Safe Attachments:
- Replaces the attachment
- Displays a malware warning notification attachment

The user is informed:
- The original attachment contained malware

---

# Block vs Dynamic Delivery

| Feature | Block | Dynamic Delivery |
|---|---|---|
| Delivers email body immediately | No | Yes |
| Delivers attachment immediately | No | Placeholder only |
| Prevents delivery of malicious emails | Yes | Yes |
| User productivity impact | Higher | Lower |
| Recommended for most organizations | No | Yes |
| Best for high-security environments | Yes | Sometimes |

---

# Benefits of Dynamic Delivery

## Security Benefits
- Malware scanning still occurs
- Unsafe attachments remain blocked

---

## Productivity Benefits
Users can:
- Read emails immediately
- Reply while scanning occurs
- Continue working without waiting for attachment analysis

---

# Key Takeaways
- Safe Attachments protects users from malicious attachments.
- Block mode completely prevents message delivery when malware is detected.
- Dynamic Delivery is Microsoft's recommended option for most organizations.
- Dynamic Delivery balances:
  - Security
  - User productivity
  - Faster email experience
- Users receive placeholder attachments while scanning occurs in the background.
