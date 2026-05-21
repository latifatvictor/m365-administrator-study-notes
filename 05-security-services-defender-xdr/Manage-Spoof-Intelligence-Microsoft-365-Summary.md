# Manage Spoof Intelligence in Microsoft 365

## Overview

Spoof intelligence is a Microsoft Defender for Office 365 feature that helps organizations:
- Detect spoofed senders
- Reduce phishing attacks
- Identify legitimate spoofing scenarios
- Reduce false positives

Spoof intelligence works with:
- SPF
- DKIM
- DMARC
- Composite authentication

to determine whether spoofed messages should be:
- Allowed
- Blocked

---

# What is Spoofing?

Spoofing occurs when:
- A sender appears to be someone else

Attackers spoof:
- Internal domains
- External domains
- Trusted companies
- Legitimate users

Goal:
- Deliver spam
- Launch phishing attacks
- Steal credentials
- Trick users into trusting messages

---

# Legitimate Spoofing Scenarios

Some spoofing scenarios are valid business operations.

---

# Legitimate Internal Domain Spoofing

Examples:
- Third-party poll providers sending company mail
- External marketing companies sending updates
- Assistants sending email on behalf of executives
- Internal applications sending notifications

---

# Legitimate External Domain Spoofing

Examples:
- Mailing lists/discussion lists
- SaaS applications sending reports
- External companies sending on behalf of another organization

---

# Purpose of Spoof Intelligence

Spoof intelligence helps organizations:
- Identify trusted spoofed senders
- Reduce false positives
- Block malicious spoofing attempts
- Improve phishing protection

---

# Spoof Intelligence and Authentication

Spoof intelligence analyzes senders that:
- Fail SPF
- Fail DKIM
- Fail DMARC

but may still:
- Pass Microsoft composite authentication checks

---

# Composite Authentication

Composite authentication:
- Combines multiple authentication signals
- Evaluates sender legitimacy
- Helps Microsoft determine whether messages are safe

---

# Microsoft Defender Portal Access

To manage spoof intelligence, users must belong to one of these roles:

## Organization Management

## Security Administrator
PLUS:
- View-Only Configuration
OR
- View-Only Organization Management

---

# Read-Only Access Roles

## Global Reader

## Security Reader

---

# Default Setting

Spoof intelligence is:
- Enabled by default

Configured through:
- Anti-phishing policies

---

# Open Spoof Intelligence Insight

Navigate to:
```text
Microsoft Defender Portal
→ Email & Collaboration
→ Policies & Rules
→ Threat Policies
→ Tenant Allow/Block Lists


Spoof intelligence in Microsoft Defender for Office 365 helps organizations detect and manage spoofed email senders. It identifies messages that fail SPF, DKIM, or DMARC checks and determines whether they are legitimate or malicious using Microsoft composite authentication.

Organizations can:
- Allow trusted spoofed senders
- Block malicious spoofed senders
- Reduce false positives
- Investigate spoofing activity

Spoof intelligence is enabled by default and is managed in the Microsoft Defender portal under:
```text
Email & Collaboration → Policies & Rules → Threat Policies → Tenant Allow/Block Lists
