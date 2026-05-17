# Implement Microsoft Entra Smart Lockout

## Overview

Microsoft Entra Smart Lockout:
- Protects accounts from brute-force attacks
- Detects malicious sign-in attempts
- Differentiates between valid users and attackers

Smart Lockout:
- Blocks attackers
- Minimizes disruption for legitimate users



---

# Purpose of Smart Lockout

Smart Lockout helps:
- Prevent password guessing attacks
- Stop brute-force attacks
- Protect cloud and hybrid identities
- Improve authentication security

---

# Default Smart Lockout Settings

By default:
- Account locks after 10 failed attempts
- Initial lockout duration = 1 minute (60 seconds)

---

# Lockout Behavior

## After 10 Failed Attempts

- User account becomes temporarily locked

---

# Successive Failed Attempts

After each additional failed attempt:
- Lockout duration increases

Examples:
- 11th failed attempt = another 1-minute lockout
- 12th failed attempt = longer lockout duration

---

# Password Hash Tracking

Smart Lockout:
- Tracks previous failed passwords
- Remembers last three failed password attempts

---

# Benefit of Password Tracking

If attacker repeatedly uses:
- Same incorrect password

Then:
- Lockout counter does NOT increase

This prevents:
- Accidental user lockouts
- Simple denial-of-service lockout attacks

---

# Smart Lockout Availability

Smart Lockout:
- Is enabled by default
- Available for all Microsoft Entra ID customers

---

# Licensing Requirements

## Default Configuration

Included for:
- All Microsoft Entra customers

---

# Custom Configuration

Requires:
- Paid Microsoft Entra licenses

Examples:
- Microsoft Entra ID P1
- Microsoft Entra ID P2

---

# Genuine Users vs Attackers

Smart Lockout:
- Attempts to identify legitimate users
- Uses intelligent detection mechanisms

Goal:
- Block attackers
- Allow genuine users continued access

---

# Familiar vs Unfamiliar Locations

Smart Lockout:
- Uses location awareness

Tracks:
- Familiar locations
- Unfamiliar locations

Each location type:
- Has separate lockout counters

---

# Multi-Datacenter Lockout Tracking

Each Microsoft Entra datacenter:
- Tracks lockout independently

---

# Lockout Calculation

Smart Lockout calculates attempts using:

threshold_limit × datacenter_count

Example:
- Threshold = 10
- Two datacenters
- Effective threshold = 20 attempts

---

# Hybrid Environment Integration

Smart Lockout supports:
- Hybrid identity environments

Protects:
- On-premises Active Directory accounts
- Cloud identities

---

# Hybrid Protection Benefits

Smart Lockout:
- Filters attacks before reaching on-premises AD
- Reduces on-premises account lockouts

Works with:
- Password Hash Sync (PHS)
- Pass-Through Authentication (PTA)

---

# Smart Lockout with Pass-Through Authentication (PTA)

## Important Considerations

PTA authentication:
- Occurs on-premises
- Not in the cloud

---

# PTA Limitation

Password hash tracking:
- Is NOT available with PTA

---

# Recommended Lockout Configuration

Microsoft recommends:
- Microsoft Entra threshold lower than AD threshold

---

# Best Practice

On-premises AD lockout threshold:
- Should be 2–3 times higher than Microsoft Entra threshold

---

# Lockout Duration Recommendation

Microsoft Entra lockout duration:
- Should be longer than Active Directory reset duration

---

# Example Configuration

Example:
- Microsoft Entra lockout duration = 120 seconds
- Active Directory reset counter = 60 seconds

This ensures:
- Cloud filtering happens before on-premises lockout

---

# Important Warning

Microsoft Entra:
- Uses seconds for lockout duration

Active Directory:
- Uses minutes

Administrators must:
- Avoid configuration mistakes

---

# Unlocking Locked Accounts

If Smart Lockout triggers:
- Administrator must wait for expiration

OR

User can:
- Use Self-Service Password Reset (SSPR)

---

# SSPR Recovery

Users can unlock accounts using:
- Trusted devices
- Trusted locations

---

# Verify On-Premises Lockout Policy

## Steps

1. Open Group Policy Management
2. Edit relevant Group Policy
3. Navigate to:

Computer Configuration  
→ Policies  
→ Windows Settings  
→ Security Settings  
→ Account Policies  
→ Account Lockout Policy

4. Verify:
- Account lockout threshold
- Reset account lockout counter

---

# Managing Smart Lockout Settings

## Configuration Path

Microsoft Entra admin center:

Protection  
→ Authentication methods  
→ Password protection

---

# Configurable Settings

Administrators can configure:
- Lockout threshold
- Lockout duration

---

# Lockout Threshold

Defines:
- Number of failed attempts before lockout

Default:
- 10 failed attempts

---

# Lockout Duration

Defines:
- Length of lockout in seconds

Default:
- 60 seconds

---

# Repeated Lockouts

If first attempt after unlock fails:
- Account locks again immediately

Repeated failures:
- Increase lockout duration further

---

# Smart Lockout Error Message

When triggered, users see:

“Your account is temporarily locked to prevent unauthorized use. Try again later, and if you still have trouble, contact your admin.”

---

# Security Benefits of Smart Lockout

Benefits include:
- Protection against brute-force attacks
- Reduced credential attacks
- Reduced on-premises lockouts
- Better user experience
- Intelligent attack filtering

---

# Smart Lockout Best Practices

Microsoft recommends:
- Enable MFA
- Configure proper thresholds
- Use hybrid protections
- Enable SSPR
- Monitor authentication activity

---

# Smart Lockout and Zero Trust

Supports Zero Trust by:
- Verifying authentication attempts
- Blocking suspicious activity
- Protecting identities proactively

---

# Key Takeaways

Microsoft Entra Smart Lockout:
- Protects against password attacks
- Differentiates between attackers and genuine users
- Is enabled by default

Key features:
- Intelligent lockout detection
- Password hash tracking
- Familiar location awareness
- Hybrid identity protection

Best practices:
- Configure proper thresholds
- Use MFA
- Enable SSPR
- Align Entra and AD lockout settings

