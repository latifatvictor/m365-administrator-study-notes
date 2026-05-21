# Expand EOP Protections by Using Safe Attachments and Safe Links

## Overview

Exchange Online Protection (EOP) provides:
- Frontline email protection
- Spam filtering
- Malware filtering
- Phishing protection

Microsoft Defender for Office 365 extends EOP protections using:
1. Safe Attachments
2. Safe Links

These features provide:
- Advanced threat protection
- Zero-day attack protection
- Sandbox analysis
- Time-of-click protection

---

# Safe Attachments

## Purpose

Safe Attachments protects users from:
- Malicious email attachments
- Unknown malware
- Zero-day threats

---

# How Safe Attachments Works

## Step 1

Email arrives with attachment.

---

# Step 2

Safe Attachments:
- Removes attachment temporarily
- Sends attachment to Microsoft servers

---

# Step 3

Microsoft opens attachment in:
- Virtual environment
- Sandboxed environment

Purpose:
- Analyze suspicious behavior safely

---

# Step 4

Microsoft evaluates:
- File behavior
- Suspicious activity
- Malware indicators

---

# If Attachment is Safe

Microsoft:
- Delivers email and attachment to mailbox

User:
- Opens file normally

---

# If Attachment is Malicious

Microsoft:
- Blocks attachment
- Removes malicious file
- Moves email to Junk Email folder
- Warns user about threat

---

# Advanced Safe Attachments Protection

Safe Attachments also uses:
- Machine learning
- Artificial intelligence
- Threat intelligence

Purpose:
- Detect new and emerging threats

---

# Unknown Suspicious Files

If Microsoft suspects:
- File may be malicious

then:
- Security experts perform deeper analysis

---

# Safe Attachments Benefits

Safe Attachments helps:
- Stop malware infections
- Detect zero-day malware
- Prevent ransomware delivery
- Protect user devices
- Reduce phishing payload risks

---

# Safe Links

## Purpose

Safe Links protects users from:
- Malicious URLs
- Phishing websites
- Dangerous redirects
- Zero-day link attacks

---

# How Safe Links Works

## Step 1

User clicks a link in:
- Email
- Documents
- Teams
- Other Microsoft 365 content

---

# Step 2

Safe Links sends URL to:
- Microsoft 365 servers

---

# Step 3

Microsoft checks URL against:
- Known malicious URL database
- Threat intelligence feeds

---

# If URL is Malicious

Microsoft:
- Blocks access
- Displays warning page
- Prevents user from visiting site

---

# If URL is Unknown

Safe Links:
- Opens URL in virtual environment
- Analyzes suspicious behavior

---

# If URL is Safe

Microsoft:
- Redirects user to original website

---

# Safe Links URL Rewriting

Safe Links:
- Rewrites URLs with unique identifiers

Purpose:
- Track links
- Reevaluate links later
- Block links if they become malicious later

---

# Time-of-Click Protection

Safe Links checks URLs:
- At the moment user clicks

This protects users even if:
- Link becomes malicious AFTER delivery

---

# Zero-Day Protection

Safe Links protects against:
- Newly created malicious URLs
- Previously unknown threats

---

# Safe Links Benefits

Safe Links helps:
- Prevent phishing attacks
- Block malicious websites
- Stop credential theft
- Protect against zero-day attacks
- Improve Microsoft 365 security posture

---

# EOP + Defender for Office 365 Pipeline

## EOP First Layer

Provides:
- Spam filtering
- Malware filtering
- Anti-phishing
- Anti-spoofing

---

# Defender for Office 365 Second Layer

Adds:
- Safe Attachments
- Safe Links
- Sandbox analysis
- Behavioral detection

---

# Security Technologies Used

| Technology | Purpose |
|---|---|
| Sandbox | Safely analyze files/URLs |
| Machine Learning | Detect suspicious behavior |
| Artificial Intelligence | Identify emerging threats |
| Threat Intelligence | Detect known malicious activity |
| URL Rewriting | Enable time-of-click protection |

---

# Key Security Concepts

| Concept | Meaning |
|---|---|
| Safe Attachments | Sandboxes email attachments |
| Safe Links | Protects against malicious URLs |
| Sandbox | Isolated virtual environment |
| Zero-Day Attack | Previously unknown threat |
| Time-of-Click Protection | URL checked when clicked |

---

# Comparison: Safe Attachments vs Safe Links

| Feature | Safe Attachments | Safe Links |
|---|---|---|
| Protects against | Malicious files | Malicious URLs |
| Uses sandboxing | Yes | Yes |
| Uses machine learning | Yes | Yes |
| Protects against zero-day threats | Yes | Yes |
| Time-of-click protection | No | Yes |
| URL rewriting | No | Yes |

---

# Best Practices

Microsoft recommends:
- Enable Safe Attachments
- Enable Safe Links
- Use Defender for Office 365
- Configure SPF, DKIM, and DMARC
- Educate users about phishing
- Monitor Defender reports regularly
- Use layered email security

---

# Security Benefits

Safe Attachments and Safe Links help organizations:
- Prevent malware infections
- Block phishing attacks
- Detect suspicious behavior
- Protect users from zero-day attacks
- Reduce ransomware risk
- Improve Microsoft 365 email security

---

# Important Exam Points

| Topic | Key Point |
|---|---|
| Safe Attachments | Sandboxes email attachments |
| Safe Links | Protects URLs at click time |
| Safe Links rewriting | Enables future URL blocking |
| Sandbox | Isolated testing environment |
| Zero-day attack | Unknown/new threat |
| Time-of-click protection | Checks links when clicked |

---

# Final Summary

Microsoft Defender for Office 365 enhances Exchange Online Protection (EOP) using:
- Safe Attachments
- Safe Links

Safe Attachments:
- Analyzes email attachments in sandbox environments
- Blocks malicious files
- Protects against zero-day malware

Safe Links:
- Analyzes URLs
- Rewrites links
- Provides time-of-click protection
- Blocks malicious websites

Together, these technologies provide:
- Advanced threat protection
- Zero-day protection
- Improved phishing defense
- Stronger Microsoft 365 email security.

---

# Knowledge Check Concepts

## Safe Attachments
Protects against malicious email attachments.

## Safe Links
Protects users from malicious URLs.

## Sandbox
Virtual isolated environment used for analysis.

## Time-of-Click Protection
Checks URLs when users click them.

---

# File Reference

Source notes uploaded by user: 
