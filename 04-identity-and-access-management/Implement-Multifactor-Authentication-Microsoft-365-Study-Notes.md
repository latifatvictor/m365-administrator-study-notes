# Implement Multifactor Authentication (MFA)

## Overview

Microsoft Entra Multifactor Authentication (MFA) increases security by requiring users to provide more than one authentication factor during sign-in.

MFA helps protect organizations against:
- Password theft
- Phishing attacks
- Credential compromise
- Unauthorized access

Source: :contentReference[oaicite:0]{index=0}

---

# Why MFA is Important

Passwords are:
- Commonly reused
- Often weak
- Vulnerable to phishing
- Vulnerable to password spraying attacks

MFA adds:
- An extra verification step

Even if attackers steal passwords:
- They still need the second authentication factor

---

# Authentication Factors

MFA uses multiple authentication categories:

## Something You Know
Examples:
- Password
- PIN

---

# Something You Have
Examples:
- Mobile phone
- Security key
- Hardware token

---

# Something You Are
Examples:
- Fingerprint
- Facial recognition
- Biometrics

---

# How MFA Works

## Step 1

User enters:
- Username
- Password

---

# Step 2

System verifies:
- Credentials

---

# Step 3

System requests:
- Second authentication factor

---

# Step 4

User approves:
- Phone notification
- OTP code
- Biometric verification

---

# Step 5

If both factors are valid:
- Access granted

---

# MFA Security Benefits

MFA:
- Prevents unauthorized access
- Reduces account compromise
- Protects sensitive data
- Supports Zero Trust security

---

# Supported MFA Methods

## Phone Call Verification

Users receive:
- Automated phone call

Users:
- Confirm identity during call

---

# Text Message Verification

Users receive:
- SMS code

Users:
- Enter verification code

---

# Microsoft Authenticator App

Supports:
- Push notifications
- One-time passcodes

Benefits:
- Secure
- Convenient
- Recommended by Microsoft

---

# OATH Hardware Tokens

Physical devices that:
- Generate one-time passwords (OTP)

Useful for:
- Users without smartphones

---

# FIDO2 Security Keys

Physical security keys that support:
- Passwordless authentication

Benefits:
- Strong phishing resistance
- Fast authentication

---

# Third-Party Authenticator Apps

Supported apps include:
- Google Authenticator
- Authy

Requirement:
- Must support TOTP protocol

---

# Conditional Access and MFA

Conditional Access can:
- Dynamically require MFA

Based on:
- User location
- Device compliance
- Risk level
- Application
- Sign-in behavior

---

# MFA Enablement Options

Microsoft 365 provides three main ways to enable MFA:

1. Conditional Access Policies
2. Security Defaults
3. Legacy Per-User MFA

---

# Conditional Access MFA

## Recommended by Microsoft

Conditional Access provides:
- Granular MFA control
- Risk-based authentication
- Flexible policy targeting

---

# Conditional Access Example

Policy example:
- Require MFA for administrators

Conditions:
- User group membership
- Device state
- Application access

---

# Benefits of Conditional Access MFA

Conditional Access enables:
- Context-aware authentication
- Better security
- Better user experience
- Advanced controls

---

# Supported Licenses for Conditional Access

Required licenses:
- Microsoft 365 Business Premium
- Microsoft 365 E3/E5
- Microsoft Entra ID P1/P2

---

# Common Conditional Access MFA Policies

Microsoft recommends:
- Require MFA for administrators
- Require MFA for all users
- Block legacy authentication

---

# Risk-Based MFA

With Microsoft Entra ID Protection:
- MFA can trigger automatically based on risk

Examples:
- Medium risk sign-ins
- High risk sign-ins

---

# Risk-Based MFA Licensing

Requires:
- Microsoft Entra ID P2
- Microsoft 365 E5

---

# Security Defaults

## Overview

Security Defaults:
- Automatically enable baseline security protections

Features include:
- MFA enforcement
- Blocking legacy authentication
- MFA registration requirements

---

# Security Defaults Advantages

Benefits:
- Easy to configure
- Minimal administration
- Strong baseline security

---

# Security Defaults Limitations

Security Defaults:
- Cannot be customized
- Apply to all users equally

Potential issues:
- User inconvenience
- No granular policy control

---

# Best Use Cases for Security Defaults

Recommended for:
- Small businesses
- Organizations with limited IT resources
- Quick MFA deployment

---

# Enable Security Defaults

## Steps

1. Open Microsoft Entra admin center
2. Select Overview
3. Open Properties
4. Select Manage Security Defaults
5. Enable Security Defaults
6. Save changes

---

# Legacy Per-User MFA

## Overview

Per-user MFA:
- Enables MFA individually for users

Microsoft recommendation:
- Avoid for large organizations

---

# Advantages of Per-User MFA

Useful for:
- Small organizations
- Quick deployments
- Testing environments

---

# Disadvantages of Per-User MFA

Problems include:
- Difficult management
- Increased administrative effort
- Inconsistent policies
- Risk of misconfiguration

---

# Legacy Authentication Risk

Per-user MFA:
- Does NOT fully block legacy authentication

Legacy protocols include:
- SMTP
- IMAP
- POP3

Attackers can exploit:
- Legacy authentication bypass

---

# Why Conditional Access is Better

Conditional Access provides:
- Context-aware decisions
- Centralized policy management
- Better scalability
- Better security consistency

---

# Enable Per-User MFA

## Steps

1. Open Microsoft 365 admin center
2. Select Settings
3. Select Org settings
4. Select Multifactor authentication
5. Configure users

---

# Per-User MFA Options

Administrators can:
- Enable MFA
- Disable MFA
- Reset MFA settings
- Delete app passwords
- Reset remembered devices

---

# Bulk MFA Updates

Administrators can:
- Use CSV import

CSV supports:
- Enable MFA
- Disable MFA

Useful for:
- Large user updates

---

# Service Settings for MFA

Global MFA settings include:
- App passwords
- Trusted IPs
- Verification methods
- Trusted devices

---

# App Passwords

Administrators can:
- Allow app passwords
- Block app passwords

App passwords are used for:
- Older non-browser applications

---

# Trusted IPs

Organizations can:
- Skip MFA from trusted locations

Examples:
- Corporate offices
- VPN ranges

---

# Verification Options

Organizations can enable:
- Phone call
- Text message
- Mobile app notifications
- Mobile app verification codes
- Hardware token codes

---

# Remember MFA on Trusted Devices

Users can:
- Skip MFA prompts temporarily

Configurable duration:
- 1 to 365 days

Default:
- 90 days

---

# Sign-In Frequency Recommendations

Microsoft recommends:
- Using Conditional Access sign-in frequency policies

Benefits:
- Better user experience
- Reduced MFA fatigue
- Improved security balance

---

# Risks of Excessive MFA Prompts

Too many prompts can:
- Reduce productivity
- Increase user frustration
- Encourage unsafe behaviors
- Increase phishing susceptibility

---

# Best Practices for MFA

Microsoft recommends:
- Enable MFA for all administrators
- Use Conditional Access
- Block legacy authentication
- Use Microsoft Authenticator
- Use risk-based policies
- Minimize authentication fatigue

---

# Recommended Enterprise MFA Strategy

For enterprises:
- Use Conditional Access
- Use risk-based authentication
- Enable MFA for privileged roles
- Require compliant devices
- Use phishing-resistant authentication

---

# Passwordless Authentication Support

MFA supports passwordless methods such as:
- FIDO2 keys
- Biometrics
- Microsoft Authenticator

Benefits:
- Better security
- Better user experience
- Reduced password dependency

---

# MFA and Zero Trust

MFA is a core Zero Trust principle.

Zero Trust assumes:
- No sign-in is automatically trusted

Every access request must be:
- Verified
- Validated
- Continuously assessed

---

# Key Takeaways

Microsoft Entra MFA:
- Strengthens identity security
- Reduces password-based attacks
- Supports multiple authentication methods
- Integrates with Conditional Access
- Supports Zero Trust architecture

Microsoft recommends:
- Conditional Access MFA for enterprises
- Security Defaults for small businesses
- Avoiding legacy per-user MFA for large environments

