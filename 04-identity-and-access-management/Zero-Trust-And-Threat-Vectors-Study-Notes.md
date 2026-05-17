
# Explore Today’s Work and Threat Landscape

## Overview

Most cyberattacks follow a common process known as the:
- Kill Chain

Attackers move through multiple stages to:
- Gain access
- Escalate privileges
- Steal data
- Maintain persistence

Organizations should implement security controls at every stage to:
- Reduce attack success
- Limit damage
- Detect threats early

---

# Modern Threat Landscape

The global threat landscape has evolved dramatically due to:
- Cloud computing
- Remote work
- Mobile devices
- BYOD environments
- Sophisticated attack techniques

Organizations must now protect:
- Users
- Devices
- Applications
- Identities
- Data
- Cloud services

---

# Challenges Organizations Face

Modern organizations struggle with:
- Protecting sensitive data
- Managing cloud applications
- Controlling unmanaged devices
- Monitoring third-party applications
- Enforcing security policies consistently

Data now exists:
- On-premises
- In cloud services
- On mobile devices
- Across SaaS applications

---

# Microsoft’s Security Focus

Microsoft helps organizations:
- Protect against attacks
- Detect threats
- Respond quickly
- Secure identities
- Secure data
- Secure devices

---

# Examine How Phishing Retrieves Sensitive Information

## What is Phishing?

Phishing is a social engineering attack where attackers:
- Pretend to be trusted entities
- Trick users into revealing sensitive information

Examples:
- Passwords
- Credit card details
- MFA codes
- Banking information

---

# Common Phishing Characteristics

Phishing emails often:
- Appear legitimate
- Use trusted branding
- Contain fake URLs
- Create urgency
- Request immediate action

---

# Malware Payloads Delivered Through Phishing

Phishing attacks may install malware such as:

## Virus
A virus:
- Replicates itself
- Infects other files
- Modifies programs

## Trojan Horse
A trojan:
- Creates backdoors
- Installs malicious software
- Steals credentials
- Infects network devices

## Rootkit
A rootkit:
- Provides administrative access
- Hides malware
- Enables stealth attacks

## Spyware
Spyware:
- Collects user activity
- Captures keystrokes
- Tracks passwords
- Delivers ads

---

# Spear Phishing

Spear phishing:
- Targets specific individuals
- Often targets executives
- Uses personalized information
- Aims for financial gain or compromise

---

# Key Phishing Indicators

Users should watch for:
- Suspicious links
- Fake domains
- Unexpected attachments
- Urgent language
- Requests for credentials

---

# Knowledge Check

Question:
Which payload can malware deliver?

Correct Answer:
- Spyware

---

# Examine How Spoofing Deceives Users and Compromises Data Security

## What is Spoofing?

Spoofing occurs when attackers:
- Forge sender identities
- Pretend to be trusted users or domains

The goal is usually:
- Phishing
- Fraud
- Credential theft
- Malware delivery

---

# Legitimate Spoofing Scenarios

Some valid scenarios include:
- Marketing providers sending on behalf of companies
- Mailing lists relaying messages
- Assistants sending emails for executives

---

# SMTP Addresses Used in Spoofing

SMTP messages contain:
- 5321.MailFrom (Return-Path)
- 5322.From (Displayed sender)

Attackers manipulate these fields to:
- Impersonate trusted senders

---

# Exchange Online Protection (EOP)

Microsoft 365 uses:
- Exchange Online Protection (EOP)

to:
- Detect spoofing
- Prevent phishing
- Filter malicious mail

---

# Spoof Intelligence

Spoof intelligence:
- Identifies suspicious senders
- Helps distinguish legitimate spoofing from malicious spoofing

---

# Compare Spam and Malware

## Spam

Spam:
- Unwanted email
- Usually harmless
- Reduces productivity

---

# Malware

Malware is:
- Malicious software

Often delivered through:
- Attachments
- Embedded links
- Infected websites

---

# Malware Delivery Stages

## Stage 1
User:
- Opens malicious file
- Clicks malicious link

Attackers exploit:
- JavaScript
- Macros

to deploy malware.

## Stage 2
Payload is installed.

---

# Common Malware Payloads

Examples include:
- Viruses
- Trojans
- Spyware
- Rootkits

---

# Knowledge Check

Question:
What else do attackers use with JavaScript to plant malware payloads?

Correct Answer:
- Macros

---

# Examine Elevation of Privilege Attacks

## What is Elevation of Privilege?

Attackers:
- Increase permissions
- Attempt to gain admin access

Common targets:
- Global Administrator accounts
- Service administrators

---

# Common Attacker Behaviour

Attackers often:
- Create hidden admin accounts
- Promote accounts to Global Admin
- Maintain persistence silently

---

# Preventing Elevation of Privilege

Microsoft recommends:
- Enabling MFA
- Limiting Global Admin accounts
- Monitoring admin activity
- Reviewing permissions regularly

---

# Global Administrator Recommendations

Microsoft recommends:
- Minimum: 2 Global Admins
- Maximum: 5 Global Admins

---

# Signs of Compromise

Organizations should investigate:
- New admin accounts
- Permission changes
- Mail forwarding rules
- Transport rules
- Delegate permissions

---

# Knowledge Check

Question:
What helps prevent elevation of privilege attacks?

Correct Answer:
- Microsoft Entra multifactor authentication

---

# Examine How Data Exfiltration Moves Data Out of Your Tenant

## What is Data Exfiltration?

Data exfiltration is:
- Unauthorized data transfer
- Theft of sensitive information

---

# Attacker Goals

Attackers may:
- Steal intellectual property
- Sell data
- Blackmail organizations
- Maintain persistence

---

# Types of Data at Risk

Sensitive data includes:
- Emails
- Documents
- Chats
- Directory information
- Financial records

---

# Preventing Data Exfiltration

## Access Control Lists (ACLs)
Limit access to:
- Authorized users only

---

# Least Privilege

Grant:
- Minimum required permissions

---

# External Sharing Policies

Restrict:
- External data sharing
- Anonymous access

---

# Data Classification

Classify data by sensitivity:
- High business impact
- Medium business impact
- Low business impact

---

# Data Loss Prevention (DLP)

Microsoft Purview DLP helps:
- Prevent sensitive data leakage
- Detect risky behaviour
- Block policy violations

Examples:
- Credit card numbers
- National insurance numbers
- Bank details

---

# Monitoring and Detection

Organizations should enable:
- Auditing
- Alerts
- Threat analytics
- Security monitoring

---

# Adopt a Zero Trust Approach

## Zero Trust Overview

Zero Trust assumes:
- Breaches are inevitable
- No implicit trust exists

Every request must be:
- Verified
- Authenticated
- Authorized continuously

---

# Four Key Zero Trust Areas

1. Identity
2. Security
3. Compliance
4. Skilling

---

# Identity: The Starting Point

Identity is:
- The frontline of defense

Microsoft recommends:
- Strong authentication
- Device protection
- Credential protection

---

# Microsoft Entra ID Features

## Passwordless Authentication

Users can sign in using:
- Windows Hello for Business
- Microsoft Authenticator
- FIDO2 security keys

Benefits:
- Eliminates password attacks
- Improves security

---

# Conditional Access

Conditional Access:
- Evaluates risk
- Applies access policies dynamically

It uses:
- User identity
- Device state
- App sensitivity
- Risk signals

---

# Verifiable Credentials

Verifiable credentials:
- Confirm identity claims
- Improve privacy
- Reduce data storage risks

---

# Security: Assume Breach

Microsoft’s security approach:
- Assumes compromise
- Uses integrated protection platforms

---

# Microsoft Defender XDR

Microsoft Defender XDR provides:
- Unified alerts
- Automated investigations
- Threat analytics
- Cross-platform protection

---

# Microsoft Sentinel

Microsoft Sentinel:
- Provides SIEM and SOAR capabilities
- Monitors multicloud environments
- Detects threats centrally

---

# Secured-Core Systems

Secured-core systems provide:
- Firmware protection
- Hardware security
- OS-level protections

---

# Compliance: Protect from the Inside Out

Microsoft Purview helps:
- Protect data
- Classify information
- Reduce insider risk

---

# Insider Risk Management

Microsoft Purview Insider Risk Management:
- Detects risky behaviour
- Uses machine learning
- Scans audit logs

---

# Data Loss Prevention (DLP)

DLP policies:
- Protect sensitive information
- Prevent external leakage
- Monitor risky activity

---

# Multicloud Data Governance

Microsoft Purview supports:
- AWS
- SAP
- Oracle
- Multicloud environments

---

# Skilling and Certifications

Microsoft offers certifications including:

## Security, Compliance, and Identity Fundamentals
Focus:
- Security basics

## Information Protection Administrator Associate
Focus:
- Compliance controls

## Security Operations Analyst Associate
Focus:
- Threat detection and response

## Identity and Access Administrator Associate
Focus:
- Identity management using Microsoft Entra ID

---

# Key Takeaways

Modern cybersecurity requires:
- Identity protection
- Continuous verification
- MFA
- Threat detection
- Data classification
- DLP
- Zero Trust architecture

Microsoft provides:
- Microsoft Entra ID
- Conditional Access
- Defender XDR
- Sentinel
- Purview
- Zero Trust solutions

to help organizations secure modern environments.

