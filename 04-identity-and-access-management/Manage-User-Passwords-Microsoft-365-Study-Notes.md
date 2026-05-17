# Manage User Passwords in Microsoft 365

## Overview

Microsoft 365 provides secure user access through password-based authentication and password management capabilities.

Key password management features include:
- Password expiration policies
- Resetting user passwords
- Resetting administrator passwords
- Microsoft Entra Password Protection
- Eliminating weak passwords
- Self-service password reset (SSPR)



---

# Required Administrator Roles

The following roles can manage password-related tasks:

## Full Password Management Permissions
These roles can perform all password management tasks:
- Global Administrator
- Security Administrator
- Privileged Role Administrator

---

# Password Reset Permissions

These roles can reset passwords:
- User Administrator
- Password Administrator

---

# Setting Password Expiration

## Default Password Expiration Policy

Microsoft 365 sets passwords to:
- Never expire (default setting)

Microsoft recommends this approach because:
- Frequent password changes encourage weak passwords
- Users often create predictable password variations
- Attackers can easily guess incremental changes

Examples of weak password patterns:
- Password1
- Password2
- Password3

Source: :contentReference[oaicite:1]{index=1}

---

# Microsoft Recommendation

Microsoft recommends:
- Enabling Multifactor Authentication (MFA)
instead of:
- Forced periodic password changes

Reason:
- Attackers typically use stolen credentials immediately
- Password expiration provides little containment benefit

---

# Configure Password Expiration Policy

Administrators can configure password expiration using:
- Microsoft 365 admin center

---

# Steps to Configure Password Expiration

1. Sign in to Microsoft 365 admin center
2. Select:
   - Settings
   - Org settings
3. Open:
   - Security & privacy
4. Select:
   - Password expiration policy
5. Clear:
   - Set passwords to never expire
6. Configure expiration period:
   - Between 14 and 730 days
7. Save changes

---

# What Happens When Passwords Expire?

If a password expires:

## Option 1
The user:
- Changes password at next sign-in

## Option 2
An administrator:
- Resets the password manually

---

# Resetting User Passwords

Administrators can reset passwords from:
- Active users page

Options include:
- Generate random password
- Create custom password
- Force password change at next sign-in

Source: :contentReference[oaicite:2]{index=2}

---

# Self-Service Password Reset (SSPR)

## What is SSPR?

Self-Service Password Reset allows users to:
- Reset their own passwords
- Avoid helpdesk dependency

---

# Important Note About SSPR

SSPR:
- Is NOT enabled by default

Administrators must:
- Enable it for all users
or:
- Enable it for selected groups

---

# Resetting Administrator Passwords

## Option 1: Another Admin Resets Password

The following admins can reset passwords:
- Global Administrator
- User Management Administrator
- Password Administrator

Important:
- Only another Global Administrator can reset a Global Admin password

---

# Option 2: Self-Service Password Reset

Administrators can:
- Use "Can’t access your account?" on sign-in page

Requirements include:
- Alternate email address
- Mobile phone number for verification
- SMS verification code

---

# Important Password Reset Limitation

Password reset process must complete within:
- 10 minutes

Otherwise:
- Process must restart

---

# Eliminating Bad Passwords

## Weak Password Problems

Common insecure password practices include:
- Reusing passwords
- Using simple passwords
- Using predictable substitutions

Examples:
- P@$$w0rd
- Password123
- Pa55word

---

# Microsoft Entra Password Protection

Microsoft Entra Password Protection:
- Detects weak passwords
- Blocks compromised passwords
- Blocks common password variants

Source: :contentReference[oaicite:3]{index=3}

---

# Features of Password Protection

Password Protection uses:
- Global banned password list
- Custom banned password list

It also:
- Detects character substitutions
- Blocks predictable password patterns

---

# Global Banned Password List

Microsoft automatically applies:
- Global banned password list

to:
- All Microsoft Entra tenants

---

# How Microsoft Builds the Global List

Microsoft uses:
- Security telemetry
- Real-world attack analysis
- Password spray attack data

Microsoft does NOT use:
- Third-party password breach lists

---

# Characteristics of the Global List

The global banned password list:
- Cannot be disabled
- Requires no configuration
- Automatically protects users

---

# Custom Banned Password List

Organizations can create:
- Custom banned password lists

Examples of terms to block:
- Company names
- Product names
- Office locations
- Internal abbreviations

---

# Example Custom Terms

Instead of blocking:
- Fabrikam123
- LondonHQ
- FabrikamWidget

Administrators should block:
- Fabrikam
- London
- Widget

Microsoft automatically blocks:
- Variants
- Combinations
- Character substitutions

---

# Custom List Rules

## Limits

Custom banned password list:
- Maximum 1000 entries

---

# Character Rules

Requirements:
- Minimum length: 4 characters
- Maximum length: 16 characters

---

# Case Sensitivity

The custom list is:
- Case-insensitive

---

# Common Character Substitution Detection

Microsoft detects substitutions such as:
- o → 0
- a → @

---

# Configure Custom Banned Password List

## Steps

1. Open Microsoft 365 admin center
2. Navigate to:
   - Admin centers
   - Identity
3. Open:
   - Microsoft Entra admin center
4. Select:
   - Protection
   - Authentication methods
5. Select:
   - Password protection
6. Enable:
   - Enforce custom list
7. Add banned terms
8. Save configuration

Source: :contentReference[oaicite:4]{index=4}

---

# Password Protection for Windows Server AD

Administrators can enable:
- Password protection for on-premises Active Directory

This uses:
- Same global banned password list
- Same custom banned password list

for:
- Cloud
- Hybrid
- On-premises environments

---

# Important Warning

If:
- Enable password protection on Windows Server Active Directory = No

Then:
- Password validation stops
- All passwords are accepted
- Audit events are disabled

---

# Password Spray Attacks

## What is a Password Spray Attack?

Attackers:
- Try common weak passwords
- Against many accounts

Examples:
- Password123
- Welcome1
- CompanyName123

---

# How Password Protection Helps

Microsoft Entra Password Protection:
- Blocks weak passwords
- Uses real-world telemetry
- Protects against password spraying

---

# Third-Party Password Lists

Microsoft:
- Does not rely on third-party breach lists

Instead:
- Uses real-world Microsoft security telemetry

---

# Common User Error Messages

Users may see messages such as:

- "Choose a password that's harder for people to guess."
- "We've seen that password too many times before."
- "Your password contains blocked words or patterns."

---

# Licensing Requirements

## Cloud-Only Users

### Global Banned Password List
License:
- Microsoft Entra Free

### Custom Banned Password List
License:
- Microsoft Entra Premium P1 or P2

---

# Hybrid Users (Synchronized from On-Premises AD DS)

Required license:
- Microsoft Entra Premium P1 or P2

for:
- Global banned list
- Custom banned list

---

# Key Takeaways

Microsoft 365 password security best practices include:
- Using MFA
- Avoiding frequent password expiration
- Blocking weak passwords
- Enabling SSPR
- Using Microsoft Entra Password Protection
- Implementing custom banned password lists

Strong password management helps protect against:
- Password spray attacks
- Credential theft
- Weak password exploitation

