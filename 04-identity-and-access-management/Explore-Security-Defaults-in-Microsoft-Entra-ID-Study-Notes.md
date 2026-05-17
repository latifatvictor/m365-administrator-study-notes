# Explore Security Defaults in Microsoft Entra ID

## Overview

Microsoft Entra ID includes preconfigured security settings known as:
- Security Defaults

Security Defaults provide:
- Baseline security protections
- Simplified security deployment
- Automatic enforcement of core security controls



---

# Purpose of Security Defaults

Security Defaults help organizations:
- Improve tenant security quickly
- Reduce identity-based attacks
- Protect users and administrators
- Block insecure authentication methods

---

# Features Automatically Enabled

When Security Defaults are enabled, Microsoft Entra ID automatically enables:

- Multifactor Authentication (MFA) for all users
- MFA registration enforcement
- MFA for administrators
- Protection for privileged activities
- Blocking of legacy authentication protocols

---

# Benefits of Security Defaults

Advantages include:
- Easy deployment
- No complex configuration required
- Strong baseline security
- Reduced risk of phishing and password spray attacks
- Improved identity protection

---

# Identity-Based Threats Prevented

Security Defaults help mitigate:
- Password spray attacks
- Replay attacks
- Phishing attacks
- Credential theft
- Legacy authentication abuse

---

# MFA Effectiveness

Microsoft states:
- More than 99.9% of identity-related attacks can be stopped using:
  - Multifactor Authentication (MFA)
  - Blocking legacy authentication

---

# Who Should Use Security Defaults?

Microsoft recommends Security Defaults for:

- Organizations starting with Microsoft Entra ID
- Organizations without dedicated security teams
- Organizations using free Microsoft Entra licensing
- Organizations not using Conditional Access

---

# Important Limitation

Security Defaults and Conditional Access:
- Cannot be used together

They are:
- Mutually exclusive

Organizations must choose:
- Security Defaults
OR
- Conditional Access

---

# When Security Defaults May Not Be Enough

Organizations with:
- Complex security requirements
- Advanced compliance needs
- Granular access requirements

May require:
- Microsoft Entra Premium features

---

# Advanced Features in Microsoft Entra Premium

Premium licensing includes:

- Conditional Access
- Identity Protection
- Privileged Identity Management (PIM)
- Risk-based policies
- Granular access controls

---

# Security Defaults in New Tenants

Microsoft automatically enables Security Defaults:
- For tenants created after October 22, 2019

---

# Important Deployment Warning

Before enabling Security Defaults:
- Notify users
- Prepare for MFA rollout
- Ensure modern authentication readiness

Because enabling Security Defaults:
- Immediately blocks legacy authentication
- Immediately enforces MFA

---

# How to Enable Security Defaults

## Steps

1. Sign in to Microsoft Entra admin center
2. Navigate to:
   Identity → Overview
3. Select:
   Properties
4. Under Security defaults:
   Select "Manage security defaults"
5. Set:
   Security defaults = Enabled
6. Select:
   Save

---

# Security Default Policies

## Policies Automatically Enforced

### 1. Require MFA Registration

All users:
- Must register for Microsoft Entra MFA

---

# MFA Registration Timeline

Users receive:
- 14 days to complete MFA registration

Registration begins:
- After first successful interactive sign-in

---

# Supported MFA Methods

Users can register using:
- Microsoft Authenticator app
- OATH TOTP compatible apps

---

# Registration Consequence

After 14 days:
- Users cannot sign in until MFA registration is complete

---

# 2. Require MFA for Administrators

Highly privileged roles:
- Must complete MFA every sign-in

---

# Administrator Roles Requiring MFA

Includes:
- Global Administrator
- Security Administrator
- Exchange Administrator
- SharePoint Administrator
- Conditional Access Administrator
- User Administrator
- Billing Administrator
- Helpdesk Administrator
- Authentication Administrator
- Password Administrator
- Application Administrator
- Cloud Application Administrator
- Privileged Authentication Administrator

---

# Microsoft Recommendation for Admins

Microsoft recommends:
- Separate admin accounts
- Separate productivity accounts

Purpose:
- Reduce MFA fatigue
- Improve admin security

---

# 3. Require MFA for Users When Necessary

Microsoft Entra ID intelligently determines:
- When MFA should be required

Factors include:
- Location
- Device
- User role
- Risk signals
- Activity type

---

# Benefits of Intelligent MFA

Protects:
- End users
- SaaS applications
- Tenant resources

---

# 4. Block Legacy Authentication

Security Defaults block:
- Legacy authentication protocols

---

# Legacy Authentication Examples

Includes:
- Office 2010 clients
- IMAP
- POP3
- SMTP basic authentication
- Exchange ActiveSync basic authentication

---

# Why Legacy Authentication Is Dangerous

Legacy authentication:
- Does not support MFA
- Allows attackers to bypass MFA protections

---

# Before Enabling Security Defaults

Organizations should:
- Identify legacy clients
- Migrate users to modern authentication

---

# 5. Protect Privileged Activities

Users accessing privileged Azure services:
- Must complete MFA

---

# Protected Services

Includes:
- Microsoft Entra admin center
- Azure PowerShell
- Azure CLI
- Azure Resource Manager APIs

---

# Why Privileged Protection Matters

Privileged actions:
- Can modify tenant-wide configurations
- Can impact billing and security settings

Single-factor authentication:
- Is insufficient protection

---

# Modern Authentication Warning

Pre-2017 Exchange Online tenants:
- Have modern authentication disabled by default

Organizations should:
- Enable modern authentication
- Avoid sign-in loops

---

# Microsoft Entra Connect Sync Exception

Security Defaults:
- Exclude Microsoft Entra Connect synchronization account

This account:
- Is not prompted for MFA
- Should not be used for normal operations

---

# Authentication Method Considerations

After enabling Security Defaults:
- MFA methods should remain enabled

---

# Required Authentication Methods

Supported methods:
- Microsoft Authenticator notifications
- OATH TOTP applications

---

# Important Warning About MFA Methods

Do NOT disable MFA methods:
- Could lock users out
- Could lock administrators out

---

# Emergency Access Accounts

Microsoft recommends:
- At least two emergency access accounts

Also known as:
- Backup administrator accounts

---

# Purpose of Emergency Accounts

Used when:
- Standard admin accounts fail
- MFA becomes unavailable
- Admins leave the organization

---

# Emergency Account Best Practices

Emergency accounts should:
- Have Global Administrator role
- Use strong passwords
- Be stored securely offline
- Not be used daily

---

# Optional Emergency Account Configuration

Organizations may:
- Disable password expiration
- Use PowerShell for configuration

---

# B2B Users and Security Defaults

Security Defaults apply to:
- B2B guest users
- B2B direct connect users

These users:
- Must satisfy MFA requirements

---

# MFA Status Page Note

Users protected by:
- Security Defaults
OR
- Conditional Access MFA

May appear as:
- Disabled

This behavior is normal.

---

# Conditional Access Comparison

Conditional Access provides:
- More granular controls
- More authentication options
- User exclusions
- Risk-based policies

---

# Conditional Access vs Security Defaults

| Security Defaults | Conditional Access |
|---|---|
| Simple setup | Granular control |
| Basic security | Advanced policies |
| No exclusions | Supports exclusions |
| Limited customization | Highly customizable |

---

# Disabling Security Defaults

Organizations can later:
- Disable Security Defaults
- Implement Conditional Access instead

---

# Key Takeaways

Security Defaults:
- Provide baseline Microsoft Entra security
- Automatically enforce MFA
- Block legacy authentication
- Protect privileged access

Best suited for:
- Smaller organizations
- Organizations without advanced licensing
- Organizations starting their security journey

Organizations with:
- Microsoft Entra Premium
- Complex security requirements

Should consider:
- Conditional Access
- Identity Protection
- Privileged Identity Management
