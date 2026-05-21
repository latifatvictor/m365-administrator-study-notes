# Explore Anti-Spoofing Protection Provided by Exchange Online Protection (EOP)

## Overview

Exchange Online Protection (EOP) protects Microsoft 365 organizations against:
- Spoofing
- Phishing
- Forged senders
- Credential theft attacks

EOP works for:
- Microsoft 365 organizations with Exchange Online mailboxes
- Standalone EOP organizations without Exchange Online mailboxes

---

# What is Spoofing?

Spoofing is:
- Fraudulently sending email pretending to be from a trusted source

Attackers spoof:
- Companies
- Domains
- Users
- Services

Goal:
- Trick users into trusting malicious email

---

# Relationship Between Spoofing and Phishing

Attackers commonly combine:
1. Spoofing
2. Phishing

---

# Simple Analogy

## Spoofing
Acts as:
- The bait

Makes message appear:
- Legitimate
- Trustworthy

---

# Phishing
Acts as:
- The attack method

Used to:
- Steal credentials
- Steal sensitive information
- Deliver malware

---

# Common Goals of Spoofing Attacks

Attackers attempt to:
- Steal passwords
- Steal credit card details
- Deliver malware
- Trick users into replying
- Gain unauthorized access

---

# How EOP Detects Spoofing

EOP examines:
- The From header

If EOP detects:
- Forged sender identity

it identifies message as:
- Spoofed

---

# EOP Anti-Spoofing Technologies

## 1. Email Authentication

Uses:
- SPF
- DKIM
- DMARC

Purpose:
- Validate sender legitimacy

---

# SPF (Sender Policy Framework)

Purpose:
- Validates authorized sending servers

Configured as:
- DNS TXT record

---

# DKIM (DomainKeys Identified Mail)

Purpose:
- Verifies message integrity
- Confirms sender authenticity

Uses:
- Digital signatures

---

# DMARC (Domain-based Message Authentication, Reporting, and Conformance)

Purpose:
- Align SPF and DKIM
- Define handling for failed authentication

---

# Microsoft Requirement

Microsoft 365 requires:
- Email authentication for inbound sender domains

---

# 2. Spoof Intelligence Insight

Allows organizations to:
- Review spoofed messages
- View spoof activity from past 7 days
- Allow or block senders

---

# 3. Tenant Allow/Block List

Organizations can:
- Allow spoofed senders
- Block spoofed senders
- Override spoof verdicts manually

---

# 4. Anti-Phishing Policies

Anti-phishing policies can:
- Enable/disable spoof intelligence
- Enable/disable unauthenticated sender identification
- Configure blocked sender actions

---

# Microsoft Defender for Office 365 Enhancements

Provides:
- Impersonation protection
- Real-time detections
- Threat Explorer
- Spoof detections reports

---

# How Spoofing Attacks Work

Spoofed messages try to:
- Appear legitimate
- Exploit user trust

Purpose:
- Trick users into dangerous actions

---

# Example of Credential Theft Attack

Attacker spoofs:
```text
msoutlook94@service.outlook.com
