# Enhance Exchange Online Protection with Microsoft Defender for Office 365

## Overview

Microsoft 365 protects email systems using:
- Exchange Online Protection (EOP)
- Microsoft Defender for Office 365

These services help defend against:
- Spam
- Malware
- Phishing
- Spoofing
- Zero-day attacks
- Malicious links


---

# Exchange Online Protection (EOP)

## Overview

Exchange Online Protection (EOP):
- Is Microsoft’s cloud-based email security service
- Protects Exchange Online mailboxes
- Supports hybrid and on-premises environments

---

# EOP Protection Techniques

EOP uses multiple protection layers including:

- IP reputation
- URL reputation
- Domain reputation
- Spam filtering
- Malware filtering
- Content filtering
- Connection filtering
- Spoof intelligence

---

# EOP Availability

EOP is included with:
- Exchange Online mailboxes

EOP is also available as:
- A standalone service

---

# EOP Mail Flow Process

Incoming email passes through several protection stages.

---

# 1. Connection Filtering

## Purpose

Checks:
- Sender reputation
- IP reputation

---

# Result

Most spam:
- Is blocked immediately
- Is rejected before entering the environment

---

# 2. Malware Inspection

EOP scans:
- Email messages
- Attachments

---

# Malware Detection Action

If malware is detected:
- Message is quarantined

---

# Quarantine Access

By default:
- Only administrators can access malware quarantine

Administrators can:
- Configure quarantine policies
- Define user permissions

---

# 3. Policy Filtering

EOP evaluates:
- Mail flow rules
- Transport rules

---

# Example Mail Flow Rule

Example:
- Notify a manager when email arrives from a specific sender

---

# Microsoft Purview DLP

In some environments:
- DLP checks occur during policy filtering

---

# 4. Content Filtering

Content filtering detects:

- Spam
- High confidence spam
- Phishing
- High confidence phishing
- Bulk email
- Spoofing

---

# Anti-Spam Actions

Organizations can configure actions such as:

- Quarantine
- Move to Junk Email
- Allow delivery
- Delete message

---

# Final Delivery

Messages that pass all protection layers:
- Are delivered to recipients

---

# Why Defender for Office 365 Is Important

Traditional anti-virus systems:
- Cannot effectively stop zero-day attacks

Attackers often use:
- Unknown malware signatures
- Advanced phishing campaigns

---

# Microsoft Recommendation

Microsoft recommends:
- Extending EOP using Microsoft Defender for Office 365

This provides:
- Advanced threat protection
- Better detection capabilities

---

# Microsoft Defender for Office 365

## Overview

Microsoft Defender for Office 365 protects against:

- Zero-day malware
- Advanced phishing
- Malicious URLs
- Targeted email attacks

---

# Policy Flexibility

Organizations can configure protection:
- Per user
- Per domain
- Per recipient
- Organization-wide

---

# Major Features of Defender for Office 365

Key features include:

- Safe Attachments
- Safe Links
- Spoof Intelligence
- Quarantine
- Anti-phishing policies

---

# Safe Attachments

## Purpose

Protects against:
- Zero-day malicious attachments

---

# How Safe Attachments Works

Safe Attachments:
- Opens suspicious attachments
- Uses an isolated hypervisor environment
- Analyzes behavior for malicious activity

---

# Benefit

Can detect malware:
- Before signatures exist

---

# Safe Links

## Purpose

Provides:
- Time-of-click protection

---

# How Safe Links Works

When users click links:
- URLs are checked in real time
- Malicious sites are blocked

---

# Safe Links Protection Areas

Protects links in:
- Email
- Office documents

---

# Spoof Intelligence

## Purpose

Detects:
- Spoofed senders
- Domain impersonation

---

# Administrator Actions

Admins can:
- Allow senders
- Block spoofed senders

---

# Spoof Intelligence Location

Available in:
- Microsoft Defender portal
- Anti-spam settings

---

# Quarantine

## Purpose

Stores suspicious or dangerous email safely.

---

# Messages Sent to Quarantine

Includes messages identified as:
- Spam
- Bulk mail
- Phishing
- Malware
- Mail flow rule violations

---

# Quarantine Management

Authorized users can:
- Review messages
- Delete messages
- Release messages

---

# Anti-Phishing Policies

## Purpose

Protects against:
- Commodity phishing
- Spear phishing
- Impersonation attacks

---

# Anti-Phishing Technology

Uses:
- Machine learning models
- Impersonation detection algorithms

---

# Types of Protection

Protects against:
- User impersonation
- Domain impersonation
- Credential theft attempts

---

# Microsoft Defender for Office 365 Plans

Two plans are available:

- Plan 1
- Plan 2

---

# Defender for Office 365 Plan 1

Includes:

- Safe Attachments
- Safe Links
- Safe Attachments for SharePoint, OneDrive, and Teams
- Anti-phishing protection
- Real-time detections

---

# Defender for Office 365 Plan 2

Includes everything in Plan 1 plus:

- Threat Trackers
- Threat Explorer
- Automated investigation and response
- Attack simulation training
- Advanced hunting
- Incident investigation
- Alert investigation

---

# Threat Trackers

## Purpose

Provides:
- Latest cybersecurity intelligence
- Threat trend visibility

---

# Threat Tracker Examples

Includes:
- Malware trends
- Attack campaigns
- Saved threat queries

---

# Threat Explorer

## Purpose

Provides:
- Real-time threat reporting
- Threat investigation tools

---

# Threat Explorer Benefits

Allows administrators to:
- Investigate threats quickly
- Analyze suspicious email activity
- Search historical data

---

# Attack Simulation Training

## Purpose

Allows organizations to:
- Simulate attacks safely
- Train users against phishing

---

# Simulation Examples

Includes:
- Spear phishing
- Credential harvesting
- Attachment attacks
- Password spray attacks
- Brute-force simulations

---

# Microsoft Defender XDR

Microsoft 365 Defender is now:
- Microsoft Defender XDR

XDR stands for:
- Extended Detection and Response

---

# Advanced Hunting

Defender for Office 365 Plan 2 supports:
- Advanced threat hunting

Used to:
- Investigate suspicious activity
- Detect hidden attacks
- Correlate incidents

---

# Security Benefits of Defender for Office 365

Organizations gain:
- Better email security
- Zero-day protection
- Advanced phishing protection
- URL protection
- Automated response capabilities

---

# Key Takeaways

Exchange Online Protection (EOP):
- Provides foundational email security

Microsoft Defender for Office 365:
- Extends EOP with advanced protection

Key advanced features include:
- Safe Attachments
- Safe Links
- Anti-phishing
- Spoof intelligence
- Threat investigation tools

Plan 2 adds:
- Investigation
- Automation
- Threat hunting
- Attack simulation training

