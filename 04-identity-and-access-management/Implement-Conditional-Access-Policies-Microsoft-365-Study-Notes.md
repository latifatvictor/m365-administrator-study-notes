# Implement Conditional Access Policies

## Overview

Conditional Access is a Microsoft Entra ID feature that enables administrators to control access to organizational resources based on specific conditions.

Conditional Access helps organizations:
- Protect resources from unauthorized access
- Reduce security risks
- Improve secure user productivity
- Apply access controls dynamically

Source: :contentReference[oaicite:0]{index=0}

---

# What is Conditional Access?

Conditional Access works using:
- If-Then logic

Example:
- If a user signs in from outside the corporate network,
- Then they must complete MFA.

---

# Common Conditional Access Signals

Conditional Access evaluates:
- User identity
- Device compliance
- Location
- Network
- Application
- Sign-in risk
- User risk

---

# Examples of Conditional Access Policies

## Example 1
Require:
- Multifactor Authentication (MFA)

For:
- All users within 14 days of first sign-in

---

## Example 2
Block:
- SharePoint Online
- OneDrive access

From:
- Noncompliant devices

---

## Example 3
Allow:
- Exchange Online access only through Outlook app

And require:
- App protection policy

---

# Benefits of Conditional Access

Conditional Access helps organizations:
- Protect sensitive data
- Enable secure remote work
- Reduce unauthorized access
- Improve security posture
- Control risky sign-ins

---

# Licensing Requirements

Conditional Access requires:
- Microsoft Entra Premium P1

or:
- Microsoft Entra Premium P2

Also available in:
- Microsoft 365 Business Premium

Source: :contentReference[oaicite:1]{index=1}

---

# Conditional Access and Microsoft Intune

Conditional Access integrates with:
- Microsoft Intune

This integration enables:
- Device compliance enforcement
- App protection enforcement
- Managed device validation

---

# Conditional Access and Microsoft Defender for Endpoint

Microsoft Defender for Endpoint:
- Provides device risk intelligence

Conditional Access:
- Uses this risk data to block access

---

# Example Integration Flow

1. Defender identifies device risk
2. Intune evaluates compliance
3. Conditional Access blocks risky device
4. User access is denied until remediation

---

# Device-Based Conditional Access

Organizations can require:
- Managed devices
- Compliant devices
- Hybrid-joined devices

before allowing access to:
- Microsoft 365
- SaaS apps
- On-premises apps

---

# App-Based Conditional Access

Organizations can:
- Restrict access to approved apps only

Example:
- Outlook mobile app only
- Managed applications only

---

# Common Conditional Access Signals

## User or Group Membership

Policies can target:
- Specific users
- Groups
- Roles

Examples:
- Executives
- Global Administrators
- Contractors

---

# IP Location Information

Policies can:
- Allow trusted locations
- Block risky countries
- Require MFA outside corporate network

---

# Device Information

Policies can evaluate:
- Device compliance
- Device platform
- Device risk level
- Device join status

---

# Application Information

Conditional Access can apply policies based on:
- Specific applications
- Cloud apps
- Authentication context

---

# Risk Detection

Conditional Access integrates with:
- Microsoft Entra Identity Protection

This enables:
- Risk-based access decisions
- Risk remediation workflows

---

# Microsoft Defender for Cloud Apps Integration

Conditional Access integrates with:
- Microsoft Defender for Cloud Apps

Capabilities include:
- Real-time session monitoring
- App access control
- Data protection policies

---

# Common Conditional Access Decisions

## Block Access

Most restrictive control.

Used when:
- Risk is too high
- Conditions are not met

---

# Grant Access

Least restrictive control.

Can require:
- MFA
- Compliant device
- Hybrid joined device
- Approved client app
- App protection policy

---

# Common Conditional Access Policies

Organizations commonly implement policies such as:

- Require MFA for administrators
- Require MFA for all users
- Block legacy authentication
- Block risky sign-ins
- Require compliant devices
- Require approved applications
- Require password change for risky users
- Block access from risky locations

---

# Create a Conditional Access Policy

## Step 1

Open:
- Microsoft Intune admin center

Path:
- Microsoft 365 admin center
- Show all
- Endpoint Manager

---

# Step 2

Navigate to:
- Endpoint security
- Conditional Access

---

# Step 3

Select:
- + New policy

---

# Configure Policy Assignments

## Users

Target:
- All users
- Selected groups
- Directory roles
- Guest users

---

# Target Resources

Administrators can target:
- Microsoft apps
- SaaS apps
- User actions
- Authentication contexts

Examples:
- Exchange Online
- SharePoint Online
- Azure portal

---

# Network Conditions

Policies can evaluate:
- IP ranges
- Countries/regions
- Trusted locations
- Unknown locations

---

# Trusted Locations

Trusted locations:
- Reduce unnecessary MFA prompts
- Improve risk calculation accuracy

Examples:
- Corporate headquarters
- VPN ranges
- Branch offices

---

# IP Range Rules

Important limitations:
- Maximum 195 named locations
- Maximum 2000 IP ranges per location
- CIDR masks must be greater than /8

---

# Countries/Regions Conditions

Organizations can:
- Allow or block specific countries
- Include unknown regions

Important:
- Country-based rules affect entire country
- IP ranges are more precise

---

# Conditions Section

Policies can combine:
- Device risk
- Location
- Sign-in risk
- Device compliance

to create:
- Fine-grained access control

---

# Access Controls

## Block Access

Blocks users entirely based on policy conditions.

Important:
- Must test carefully
- Can create unintended lockouts

---

# Grant Access Controls

Organizations can require:
- MFA
- Authentication strength
- Compliant device
- Hybrid joined device
- Approved app
- App protection policy
- Password change

---

# Session Controls

Conditional Access supports:
- Session restrictions
- App controls
- Sign-in frequency
- Browser persistence
- Continuous access evaluation

---

# Sign-In Frequency

Administrators can require:
- Reauthentication after specific hours/days
- Reauthentication every session

Supported apps include:
- Outlook
- Teams
- SharePoint
- Exchange Online
- Azure portal

---

# Persistent Browser Session

Allows users to:
- Stay signed in after closing browser

---

# Token Protection (Preview)

Token protection:
- Prevents token theft attacks
- Binds tokens to intended device

---

# Enable Policy Options

Policies can be set to:

## Report-only
- Evaluates policy
- Does not enforce controls

## On
- Fully enabled

## Off
- Disabled

---

# Report-Only Mode

Report-only mode helps administrators:
- Test policies safely
- Evaluate impact
- Avoid lockouts

Results appear in:
- Sign-in logs
- Conditional Access insights

---

# Authentication Strength

Authentication strength:
- Defines acceptable authentication combinations

Used to:
- Protect sensitive resources
- Require phishing-resistant methods

---

# Built-In Authentication Strengths

## Multifactor Authentication Strength

Requires:
- Two or more authentication factors

Examples:
- Password + SMS
- Smart card + PIN
- Biometrics + PIN

---

# Passwordless MFA Strength

Removes:
- Traditional passwords

Examples:
- FIDO2 keys
- Windows Hello

---

# Phishing-Resistant MFA Strength

Protects against:
- Credential phishing attacks

Examples:
- FIDO2 security keys
- Windows Hello biometrics

---

# Authentication Strength Use Cases

Organizations can:
- Require phishing-resistant MFA for sensitive apps
- Require stronger methods for risky users
- Require stronger methods outside corporate network

---

# Authentication Strength Evaluation

For successful access:
- Method must be allowed
- Method must be registered
- Method must satisfy policy requirements

---

# Multiple Policy Evaluation

When multiple policies apply:
- ALL policy conditions must be satisfied

Example:
- MFA policy
- Device compliance policy

Both requirements must pass.

---

# Combined Registration

If users lack required methods:
- Microsoft Entra redirects them to registration

Users must:
- Register at least one acceptable method

---

# Example Authentication Scenario

Scenario:
- User signs in using Password + SMS
- Resource requires MFA

Result:
- Access granted

---

# Stronger Authentication Scenario

Scenario:
- Resource requires phishing-resistant MFA
- User previously used Password + SMS

Result:
- Additional authentication required

Examples:
- Windows Hello
- FIDO2 key

---

# Key Takeaways

Conditional Access:
- Protects organizational resources
- Applies adaptive access controls
- Uses real-time security signals
- Integrates with Intune and Defender
- Supports risk-based access decisions

Best practices include:
- Requiring MFA
- Blocking legacy authentication
- Using compliant devices
- Implementing report-only mode first
- Using phishing-resistant authentication for sensitive resources

