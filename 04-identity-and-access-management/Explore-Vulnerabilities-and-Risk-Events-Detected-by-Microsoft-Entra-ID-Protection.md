# Explore the Vulnerabilities and Risk Events Detected by Microsoft Entra ID Protection

## Overview

Microsoft Entra ID Protection helps organizations:
- Detect vulnerabilities
- Detect risky user activity
- Identify compromised identities
- Prevent unauthorized access
- Improve identity security posture

It uses:
- Machine learning
- Heuristics
- Behavioral analytics
- Threat intelligence

to identify identity-related threats and suspicious activity.

---

# What is a Vulnerability?

A vulnerability is:
- A weakness attackers can exploit to gain unauthorized access or perform malicious actions.

Microsoft Entra ID Protection:
- Identifies vulnerabilities
- Recommends remediation actions
- Helps organizations improve security posture

---

# Common Vulnerabilities Detected by Microsoft Entra ID Protection

Microsoft Entra ID Protection detects:
1. Multifactor authentication registration not configured
2. Unmanaged cloud apps
3. Security alerts from Privileged Identity Management (PIM)

---

# 1. Multifactor Authentication Registration Not Configured

## Overview

This vulnerability identifies users who:
- Haven’t configured MFA

Without MFA:
- User accounts rely only on passwords
- Accounts become easier to compromise

---

# Why MFA Matters

MFA adds:
- A second authentication factor

Examples:
- Phone call
- Text message
- Authenticator app
- Verification code
- OATH token
- Biometrics

---

# Benefits of MFA

MFA:
- Reduces account compromise
- Protects applications and data
- Supports Conditional Access
- Improves identity security

---

# Recommended Action

Microsoft recommends:
- Requiring Microsoft Entra MFA for all user sign-ins

MFA is especially important for:
- Risk-based Conditional Access policies

---

# 2. Unmanaged Cloud Apps

## Overview

Organizations often:
- Don’t know all cloud apps employees are using

This is commonly called:
- Shadow IT

Examples include:
- Unauthorized SaaS apps
- Personal cloud storage
- Third-party collaboration tools

---

# Risks of Unmanaged Cloud Apps

Risks include:
- Unauthorized data access
- Data leakage
- Compliance violations
- Reduced visibility
- Security exposure

---

# Recommended Action

Microsoft recommends:
- Deploying Cloud App Discovery

Cloud App Discovery helps:
- Discover cloud applications
- Identify risky apps
- Monitor cloud usage

---

# Additional Recommendation

After discovering unmanaged apps:
- Manage them using Microsoft Entra ID

---

# 3. Security Alerts from Privileged Identity Management (PIM)

## Overview

Privileged accounts:
- Increase attack surface
- Are highly targeted by attackers

Examples:
- Global Administrators
- Exchange Administrators
- Security Administrators

---

# Risks of Excessive Privileged Access

Risks include:
- Privilege escalation
- Account takeover
- Lateral movement
- Unauthorized access

---

# Recommended Action

Microsoft recommends:
- Using Microsoft Entra Privileged Identity Management (PIM)

PIM helps organizations:
- Manage privileged identities
- Monitor privileged access
- Enforce least privilege
- Control temporary access

---

# What PIM Can Manage

PIM can manage access to:
- Microsoft Entra ID
- Microsoft 365
- Microsoft Intune
- Azure resources
- SaaS applications

---

# Risk Events Detected by Microsoft Entra ID

Microsoft Entra ID Protection detects:
- Suspicious user behavior
- Identity-related threats
- Risky sign-ins

It stores each suspicious action as:
- A risk event

---

# Six Main Risk Events

Microsoft Entra ID currently detects:

1. Users with leaked credentials
2. Sign-ins from anonymous IP addresses
3. Impossible travel to atypical locations
4. Sign-ins from infected devices
5. Sign-ins from IP addresses with suspicious activity
6. Sign-ins from unfamiliar locations

---

# Detection Types

| Detection Type | Reporting Latency |
|---|---|
| Real-time | 5 to 10 minutes |
| Offline | 2 to 4 hours |

---

# Risk Levels

| Risk Level | Description |
|---|---|
| High | High confidence compromise detected |
| Medium | Potentially risky activity |
| Low | Lower confidence suspicious activity |

---

# High Risk

High risk events:
- Strongly indicate account compromise
- Require immediate remediation

---

# Medium Risk

Medium risk events:
- Are suspicious
- May require investigation
- Could indicate compromise

---

# Low Risk

Low risk events:
- May not require immediate action
- Become more significant when combined with other events

---

# Licensing Note

Microsoft Entra Premium P2:
- Provides detailed risk event information

Microsoft Entra Premium P1:
- Provides limited detection visibility

---

# 1. Users with Leaked Credentials

## Overview

Attackers often:
- Share stolen credentials online

Credentials may appear:
- On dark web sites
- On paste sites
- On black markets

---

# How Microsoft Detects Leaked Credentials

Microsoft’s Leaked Credentials Service:
- Monitors public and dark web sources
- Works with:
  - Researchers
  - Law enforcement
  - Security teams

If stolen credentials match:
- Current Microsoft Entra user credentials

then:
- A leaked credentials risk event is created

---

# 2. Sign-Ins from Anonymous IP Addresses

## Overview

Attackers often use:
- Anonymous proxy services
- VPNs
- TOR networks

to hide their true location.

---

# Why This is Risky

Anonymous IP usage may indicate:
- Malicious intent
- Credential attacks
- Identity abuse

---

# 3. Impossible Travel to Atypical Locations

## Overview

This risk event detects:
- Impossible geographic travel patterns

---

# Example

User signs in:
- From London
- Then 30 minutes later from Tokyo

This is considered:
- Impossible travel

---

# Detection Factors

Microsoft evaluates:
- Time between sign-ins
- Travel feasibility
- User behavior history

---

# Learning Period

Initial learning period:
- 14 days

During this time:
- User behavior is learned

---

# False Positive Reduction

Microsoft ignores:
- VPN activity
- Common organizational locations
- Known trusted behavior

---

# 4. Sign-Ins from Unfamiliar Locations

## Overview

Microsoft tracks:
- Familiar locations
- Familiar IPs
- Familiar networks

If sign-in occurs from:
- New or unusual location

then:
- Risk event is triggered

---

# Learning Period

Initial learning period:
- 30 days

During this period:
- New locations are not flagged

---

# Additional Logic

Microsoft ignores:
- Familiar devices
- Nearby familiar locations

---

# Legacy Authentication Note

Basic authentication:
- Has fewer telemetry signals
- Generates more false positives

Microsoft recommends:
- Moving to modern authentication

---

# 5. Sign-Ins from Infected Devices

## Overview

This risk event detects:
- Devices infected with malware

---

# Detection Method

Microsoft correlates:
- User device IPs
- Botnet server IPs

If communication is detected:
- Risk event is generated

---

# 6. Sign-Ins from IP Addresses with Suspicious Activity

## Overview

This event identifies:
- IPs with high failed sign-in volume

across:
- Multiple accounts
- Short time periods

---

# Why This Matters

This pattern commonly indicates:
- Password spray attacks
- Brute-force attacks
- Credential stuffing

---

# Learning Period

Initial learning period:
- 14 days

Microsoft learns:
- Normal user behavior
- Normal tenant behavior

---

# Key Security Concepts

| Concept | Meaning |
|---|---|
| Vulnerability | Weakness attackers can exploit |
| Risk Event | Suspicious identity-related activity |
| User Risk | Probability account is compromised |
| Sign-In Risk | Probability sign-in is malicious |
| Shadow IT | Unmanaged cloud applications |
| PIM | Privileged Identity Management |

---

# Best Practices

Microsoft recommends:
- Enable MFA for all users
- Deploy Cloud App Discovery
- Use PIM for privileged accounts
- Monitor risky sign-ins
- Investigate leaked credentials immediately
- Use Conditional Access
- Move to modern authentication
- Reduce administrative privileges

---

# Security Benefits

Microsoft Entra ID Protection helps organizations:
- Detect account compromise
- Prevent identity attacks
- Reduce attack surface
- Improve Zero Trust security
- Monitor privileged access
- Identify risky sign-ins

---

# Exam Tips

## What Detects Shadow IT?

Answer:
- Cloud App Discovery

---

# What Helps Manage Privileged Access?

Answer:
- Microsoft Entra Privileged Identity Management (PIM)

---

# What Helps Reduce Account Compromise?

Answer:
- MFA

---

# Six Important Risk Events

1. Leaked credentials
2. Anonymous IP sign-ins
3. Impossible travel
4. Infected devices
5. Suspicious IP activity
6. Unfamiliar locations

---

# Important Learning Periods

| Detection | Learning Period |
|---|---|
| Impossible travel | 14 days |
| Suspicious IP activity | 14 days |
| Unfamiliar locations | 30 days |

---

# Final Summary

Microsoft Entra ID Protection helps organizations:
- Detect vulnerabilities
- Detect suspicious activity
- Identify risky users
- Monitor risky sign-ins
- Protect identities automatically

It uses:
- Machine learning
- Threat intelligence
- Behavioral analytics

to identify and remediate identity-based threats.

---

# Knowledge Check Answer

Q: What should Holly recommend to address unmanaged cloud apps?

Answer:
- Deploy Cloud App Discovery

---

