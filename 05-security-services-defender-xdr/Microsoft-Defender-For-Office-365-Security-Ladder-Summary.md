# Climb the Security Ladder from EOP to Microsoft Defender for Office 365

## Overview

Microsoft 365 email security is built using three layered cloud security services:

1. Exchange Online Protection (EOP)
2. Microsoft Defender for Office 365 Plan 1 (P1)
3. Microsoft Defender for Office 365 Plan 2 (P2)

Each layer:
- Builds on the previous one
- Adds more advanced protection
- Expands investigation and response capabilities

---

# Microsoft 365 Security Architecture

## EOP
Foundation security layer.

Focus:
- Basic email protection

---

# Microsoft Defender for Office 365 Plan 1

Includes:
- EOP features
PLUS:
- Advanced protection and detection

---

# Microsoft Defender for Office 365 Plan 2

Includes:
- EOP
- Defender P1
PLUS:
- Advanced investigation
- Automation
- Threat hunting
- Simulation training

---

# Security Goals Across the Products

All services support:
- Protect
- Detect
- Investigate
- Respond

However, each product emphasizes different capabilities.

---

# Exchange Online Protection (EOP)

## Main Purpose

Protects against:
- Spam
- Malware
- Phishing
- Bulk mail
- Spoofing

---

# EOP Core Technologies

## Protection Features

- Spam filtering
- Malware filtering
- Phishing detection
- Bulk mail filtering
- Spoof intelligence
- Impersonation detection
- Zero-hour auto purge (ZAP)

---

# Investigation Features

- Reports
- Audit log search
- Message trace
- Admin quarantine
- User/admin submissions

---

# Response Features

- URL allow/block lists
- File allow/block lists
- Allowlists and blocklists tuning

---

# Important EOP Note

If an organization has:
- Exchange Online mailboxes

then:
- EOP already exists automatically

---

# Email Authentication Requirement

Microsoft strongly recommends configuring:
- SPF
- DKIM
- DMARC

for all EOP deployments.

---

# Microsoft Defender for Office 365 Plan 1 (P1)

## Main Purpose

Adds:
- Advanced prevention
- Advanced detection

---

# Defender P1 Features

Includes everything in EOP PLUS:

## Safe Attachments
- Sandboxes attachments
- Detects zero-day malware

---

# Safe Links
- Time-of-click URL protection

---

# Workload Protection

Protects:
- SharePoint Online
- OneDrive
- Microsoft Teams

---

# Advanced Anti-Phishing

Adds:
- Enhanced phishing detection
- User impersonation protection
- Domain impersonation protection

---

# Alerts and SIEM Integration

Supports:
- SIEM alert integration
- Detection APIs

---

# Real-Time Detections Tool

Key Defender P1 investigation tool:
- Real-time detections

Important:
- Presence of Real-time detections indicates Defender P1

---

# Time-of-Click Protection

Protects links in:
- Email
- Office apps
- Teams

even after message delivery.

---

# Defender P1 Focus

Primary focus:
- Prevention
- Detection

---

# Microsoft Defender for Office 365 Plan 2 (P2)

## Main Purpose

Adds:
- Advanced investigation
- Threat hunting
- Automated response
- Simulation training

---

# Defender P2 Features

Includes everything in:
- EOP
- Defender P1

PLUS:

---

# Threat Explorer

Main hunting and investigation tool in P2.

Used for:
- Deep threat investigations
- Email hunting
- Threat analysis

---

# Threat Trackers

Provides:
- Information on active threat campaigns

---

# Campaign Views

Shows:
- Coordinated attack campaigns

---

# Automated Investigation and Response (AIR)

Automates:
- Investigation
- Remediation
- Response actions

---

# AIR Capabilities

Includes:
- AIR from Threat Explorer
- AIR for compromised users
- SIEM integration for automated investigations

---

# Attack Simulation Training

Allows SOC teams to:
- Simulate phishing attacks
- Train users
- Measure security awareness

---

# Advanced Hunting

Defender P2 supports:
- Advanced hunting in Microsoft Defender XDR

---

# Incident Investigation

Supports investigation of:
- Alerts
- Incidents
- Threat campaigns

inside:
- Microsoft Defender XDR

---

# Defender P2 Focus

Primary focus:
- Investigation
- Response
- Automation
- Hunting

---

# Real-Time Detections vs Threat Explorer

| Tool | Product |
|---|---|
| Real-time detections | Defender P1 |
| Threat Explorer | Defender P2 |

---

# End User Features

## EOP and Defender P1

Focus:
- User awareness

Feature:
- Report Message Outlook add-in

Users can:
- Report suspicious emails

---

# Defender P2

Focus:
- User training
- Security awareness testing

Feature:
- Threat Simulator / Attack Simulation Training

---

# Security Ladder Summary

| Product | Primary Focus |
|---|---|
| EOP | Basic protection |
| Defender P1 | Advanced prevention and detection |
| Defender P2 | Investigation, hunting, automation |

---

# Feature Comparison

| Capability | EOP | Defender P1 | Defender P2 |
|---|---|---|---|
| Spam filtering | Yes | Yes | Yes |
| Malware filtering | Yes | Yes | Yes |
| Spoof intelligence | Yes | Yes | Yes |
| Safe Attachments | No | Yes | Yes |
| Safe Links | No | Yes | Yes |
| Teams/OneDrive protection | No | Yes | Yes |
| Anti-phishing | Basic | Advanced | Advanced |
| Real-time detections | No | Yes | No |
| Threat Explorer | No | No | Yes |
| Threat Trackers | No | No | Yes |
| Automated Investigation and Response | No | No | Yes |
| Attack simulation training | No | No | Yes |
| Advanced hunting | No | No | Yes |

---

# Microsoft Defender XDR

Microsoft 365 Defender is now called:
- Microsoft Defender XDR

XDR means:
- Extended Detection and Response

---

# Key Security Concepts

| Concept | Meaning |
|---|---|
| EOP | Base email protection |
| Safe Attachments | Attachment sandboxing |
| Safe Links | Time-of-click URL protection |
| AIR | Automated Investigation and Response |
| Threat Explorer | Advanced investigation tool |
| SIEM | Security Information and Event Management |
| XDR | Extended Detection and Response |

---

# Best Practices

Microsoft recommends:
- Start with EOP configuration
- Configure SPF, DKIM, and DMARC
- Enable Safe Links
- Enable Safe Attachments
- Use Defender P2 for advanced SOC operations
- Monitor Threat Explorer regularly
- Use Attack Simulation Training
- Integrate with SIEM tools

---

# Security Benefits

These solutions help organizations:
- Block phishing attacks
- Prevent malware infections
- Detect impersonation
- Investigate threats faster
- Automate remediation
- Train users against phishing
- Improve overall security posture

---

# Important Exam Points

| Topic | Key Point |
|---|---|
| EOP | Included with Exchange Online |
| Defender P1 | Adds Safe Links and Safe Attachments |
| Defender P2 | Adds Threat Explorer and AIR |
| Real-time detections | P1 feature |
| Threat Explorer | P2 feature |
| Safe Links | Time-of-click URL protection |
| Safe Attachments | Sandboxes attachments |
| Attack Simulation Training | P2 feature |

---

# Final Summary

Microsoft 365 email security uses a layered model:

## EOP
Provides:
- Core protection against spam, malware, phishing, and spoofing.

## Defender for Office 365 Plan 1
Adds:
- Advanced prevention and detection features such as Safe Links and Safe Attachments.

## Defender for Office 365 Plan 2
Adds:
- Threat hunting
- Automated investigation
- Threat Explorer
- Attack simulation training
- Advanced response capabilities.

Organizations should:
- Configure EOP properly first
- Enable email authentication
- Expand protections using Defender for Office 365
- Use Defender P2 for advanced SOC and automation needs

to maximize Microsoft 365 security.

---

# Knowledge Check Concepts

## EOP
Foundation email security layer.

## Defender P1
Adds prevention and detection.

## Defender P2
Adds investigation and automation.

## Threat Explorer
Primary hunting tool in Defender P2.

## Real-Time Detections
Investigation tool in Defender P1.

---

