# Explore Microsoft Secure Score

## Overview

Microsoft Secure Score is a measurement of an organization’s security posture within Microsoft 365. It helps organizations understand how secure their environment is by evaluating security settings, configurations, user behaviors, and implemented protections.

The higher the Secure Score, the stronger the organization’s security posture.

Microsoft Secure Score helps organizations:

- Report on current security posture
- Improve security through recommendations
- Monitor security trends and metrics
- Compare against industry benchmarks
- Establish security KPIs
- Track progress over time

Microsoft Secure Score is available from the Microsoft Defender portal.

---

# Important Note

Microsoft Secure Score is NOT a guarantee against breaches.

It:
- Measures how many recommended security controls are implemented
- Helps reduce risk exposure
- Provides security guidance and visibility

It does NOT:
- Guarantee protection from attacks
- Predict the likelihood of compromise
- Eliminate all security risks

---

# Benefits of Microsoft Secure Score

Organizations gain access to:

- Security posture visualizations
- Trend reporting
- Real-time scoring
- Integration with Microsoft security products
- Security recommendations
- Benchmark comparisons with similar organizations

Secure Score can also recognize:
- Third-party security solutions
- Alternative mitigations

---

# How Microsoft Secure Score Works

Organizations receive points for:

- Configuring recommended security features
- Completing security-related tasks
- Implementing third-party protections
- Applying alternative mitigations

Some recommendations:
- Require full completion for full points
- Allow partial scoring based on coverage

---

# Example of Partial Scoring

Example:
- MFA recommendation worth 10 points
- 100 total users
- 50 users protected with MFA

Calculation:

50 / 100 × 10 = 5 points

This means the organization receives:
- 5 out of 10 points

---

# Secure Score Updates

Secure Score updates:
- In real time for dashboard data
- Daily for system synchronization

Important note for Microsoft Teams:
- Teams-related recommendations refresh monthly unless configuration changes occur

---

# Products Included in Secure Score

Secure Score currently supports:

- Microsoft 365
- Exchange Online
- Microsoft Entra ID
- Microsoft Defender for Endpoint
- Microsoft Defender for Identity
- Microsoft Defender for Cloud Apps
- Microsoft Teams

---

# Security Defaults

Microsoft Secure Score supports Microsoft Entra security defaults.

Security defaults provide:
- Preconfigured security protections
- Baseline protection against common attacks

When security defaults are enabled, organizations automatically receive full points for:

| Recommended Action | Points |
|---|---|
| Ensure all users can complete MFA | 9 |
| Require MFA for admin roles | 10 |
| Block legacy authentication | 7 |

---

# Important Recommendation

Microsoft recommends:
- Using security defaults
- Marking duplicate recommendations as:
  "Resolved through alternative mitigation"

This prevents duplicate security configurations.

---

# Key Secure Score Concepts

## Real-Time Security Monitoring

Secure Score:
- Continuously evaluates configurations
- Tracks implemented protections
- Displays updated posture metrics

---

# Partial Scoring

Some recommendations:
- Allow percentage-based scoring
- Measure adoption across users/devices

Example:
- MFA adoption
- Device protection coverage

---

# Third-Party Recognition

Secure Score can recognize:
- Third-party security products
- Alternative mitigations

Organizations can:
- Accept risks
- Mark mitigations as completed another way

---

# Important Security Recommendations

Common Secure Score recommendations include:

- Enable MFA
- Block legacy authentication
- Protect admin accounts
- Configure Conditional Access
- Secure endpoints
- Improve email security
- Reduce external sharing risks

---

# Knowledge Check

## Question

Which of the following statements accurately reflects Secure Score functionality?

### Correct Answer

Microsoft Secure Score represents the extent to which an organization adopted security controls in its Microsoft 365 environment

---

# Why the Other Answers Are Incorrect

## Incorrect:
"Secure Score displays the possible improvements an organization can make depending on the product licenses it owns"

Reason:
- Secure Score displays all recommendations regardless of licensing

---

## Incorrect:
"Secure Score syncs weekly to receive system data about an organization's achieved points for each action"

Reason:
- Secure Score syncs daily, not weekly

---

# Key Exam Points

## Microsoft Secure Score

Remember:
- Measures security posture
- Uses point-based recommendations
- Updates in real time
- Syncs daily
- Supports multiple Microsoft security products

---

# Security Defaults

Security defaults:
- Automatically improve Secure Score
- Enable MFA protections
- Block legacy authentication
- Provide baseline security protections

---

# Partial Scoring

Partial scoring occurs when:
- Only some users/devices are protected
- Recommendations are partially implemented

---

# Included Microsoft Products

Secure Score supports:
- Microsoft Entra ID
- Exchange Online
- Defender products
- Teams
- Microsoft 365

---

# Final Summary

Microsoft Secure Score:
- Helps organizations assess security posture
- Provides actionable recommendations
- Tracks security improvements
- Encourages best practices
- Supports continuous security monitoring

It is:
- A security measurement tool
- NOT a breach guarantee

---

# Exam Tip

Remember this simple association:

| Feature | Associated Product |
|---|---|
| Security posture measurement | Microsoft Secure Score |
| Identity protection | Defender for Identity |
| Endpoint protection | Defender for Endpoint |
| Cloud app visibility | Defender for Cloud Apps |
| Email protection | Defender for Office 365 |

---

# File Reference

Source notes uploaded by user: :contentReference[oaicite:0]{index=0}
