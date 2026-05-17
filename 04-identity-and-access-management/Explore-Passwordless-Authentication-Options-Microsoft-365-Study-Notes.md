# Explore Passwordless Authentication Options

## Overview

Passwordless authentication removes traditional passwords and replaces them with:
- Something you have
- Something you are
- Something you know

Benefits include:
- Improved security
- Better user experience
- Reduced phishing risks
- Reduced password fatigue

Source: :contentReference[oaicite:0]{index=0}

---

# Why Passwordless Authentication Matters

Traditional passwords:
- Are vulnerable to phishing
- Can be stolen
- Are often reused
- Can be weak

Passwordless authentication:
- Eliminates password exposure
- Reduces replay attacks
- Supports Zero Trust security

---

# Microsoft Passwordless Authentication Options

Microsoft Entra ID supports:

1. Windows Hello for Business
2. Platform Credential for macOS
3. Platform SSO for macOS with Smart Card
4. Microsoft Authenticator
5. Passkeys (FIDO2)
6. Certificate-Based Authentication (CBA)

---

# Windows Hello for Business

## Overview

Windows Hello for Business:
- Replaces passwords with strong authentication
- Uses device-bound credentials
- Supports biometric authentication and PINs

---

# Authentication Methods

Supported methods:
- Face recognition
- Fingerprint
- PIN

---

# Hardware Requirements

Requires:
- Trusted Platform Module (TPM)
- Windows 10 or Windows 11 device

---

# Key Security Features

Windows Hello:
- Stores credentials locally on device
- Prevents credential replay attacks
- Prevents phishing attacks
- Uses asymmetric cryptography

---

# Why PIN is Safer Than Passwords

Passwords:
- Are shared secrets
- Travel across the network
- Can be intercepted

PINs:
- Are device-specific
- Never leave the device
- Cannot be reused elsewhere

---

# Windows Hello Benefits

Benefits include:
- Passwordless sign-in
- Single sign-on (SSO)
- MFA support
- Strong phishing resistance
- Improved user experience

---

# Windows Hello Integration

Supports:
- Microsoft accounts
- Active Directory accounts
- Microsoft Entra accounts
- FIDO2-compatible services

---

# Enrollment Process

Users:
1. Complete MFA enrollment
2. Configure PIN or biometrics
3. Device creates secure credentials

---

# Windows Hello Enterprise Advantages

Provides:
- Enterprise-grade security
- Seamless authentication
- Reduced password management
- Better compliance support

---

# Platform Credential for macOS

## Overview

Platform Credential for macOS:
- Uses Secure Enclave hardware
- Enables passwordless sign-in on macOS
- Integrates with Microsoft Enterprise SSO Extension

---

# Authentication Methods

Users authenticate using:
- Touch ID
- Secure hardware-bound keys

---

# Benefits

Benefits include:
- Passwordless authentication
- Phishing-resistant authentication
- Secure Enclave protection
- Single sign-on across apps

---

# WebAuthn Support

Platform Credential supports:
- WebAuthn authentication
- Browser reauthentication scenarios

---

# FIDO2 Requirement

Administrators must:
- Enable FIDO2 authentication method

---

# Platform SSO for macOS with Smart Card

## Overview

Platform SSO for macOS:
- Uses Smart Cards
- Uses certificate-based authentication (CBA)

---

# Authentication Process

Users:
1. Sign in using smart card
2. Device unlocks
3. Microsoft Entra ID provides SSO access

---

# Supported Devices

Examples:
- Smart cards
- YubiKeys
- Smart card-compatible hardware tokens

---

# Requirements

Requires:
- Certificate-Based Authentication configured
- Microsoft Intune or supported MDM

---

# Microsoft Authenticator

## Overview

Microsoft Authenticator:
- Provides passwordless authentication
- Supports MFA
- Uses push notifications and OTP codes

---

# Supported Platforms

Available on:
- iOS
- Android

---

# Authentication Methods

Supports:
- Push notifications
- Time-based One-Time Passwords (TOTP)

---

# Push Notifications

Authentication flow:
1. User attempts sign-in
2. Notification sent to phone
3. User approves request
4. Authentication completes

---

# Benefits of Push Notifications

Advantages:
- Faster authentication
- Better security
- Better user experience
- Resistant to replay attacks

---

# Time-Based One-Time Password (TOTP)

## Overview

TOTP:
- Generates temporary codes
- Codes expire quickly
- Typically refresh every 30 seconds

---

# TOTP Security

Uses:
- Shared secret key
- Current time

Benefits:
- Temporary authentication codes
- Reduced credential theft risk

---

# Push Notifications vs TOTP

## Push Notifications

Advantages:
- Easier for users
- More secure
- Faster authentication

---

# TOTP

Useful when:
- Push notifications unavailable
- Offline authentication required

---

# Microsoft Authenticator Benefits

Benefits include:
- Strong security
- Convenient authentication
- Offline support
- Multiple account management
- Biometric support

---

# Passwordless Phone Sign-In

## Authentication Flow

User:
1. Enters username
2. Receives notification
3. Matches displayed number
4. Approves using PIN or biometrics

---

# Requirements for Authenticator Passwordless Sign-In

Requirements:
- Latest Microsoft Authenticator app
- MFA enabled
- Push notifications enabled

---

# iOS Requirements

For iOS:
- Device must be registered per tenant

---

# Android Requirements

For Android:
- Device must be registered to individual user

---

# Combined Registration Experience

To use passwordless authentication:
- Enable combined registration experience
- Enable passwordless methods

---

# Passkeys (FIDO2)

## Overview

FIDO2:
- Open passwordless authentication standard
- Developed by FIDO Alliance
- Fast IDentity Online

---

# FIDO2 Benefits

Benefits:
- Phishing-resistant
- Passwordless
- Hardware-based authentication
- Strong account protection

---

# FIDO2 Security Keys

Security keys may use:
- USB
- NFC
- Bluetooth

---

# Authentication Process

Users:
1. Insert security key
2. Verify identity
3. Access granted

---

# FIDO2 Advantages

Advantages:
- No password exposure
- Resistant to phishing
- Strong authentication
- Supports shared devices

---

# Best Use Cases for FIDO2

Ideal for:
- Shared computers
- Kiosk systems
- Highly secure environments
- Help desk environments
- Healthcare workstations

---

# FIDO2 Device Support

Supports:
- Microsoft Entra joined devices
- Hybrid joined devices
- Supported web browsers

---

# Certificate-Based Authentication (CBA)

## Overview

Certificate-Based Authentication:
- Uses X.509 certificates
- Authenticates directly against Microsoft Entra ID

---

# Key Benefits

Benefits:
- Phishing-resistant authentication
- Strong security
- Seamless Conditional Access integration

---

# CBA Authentication Flow

Authentication uses:
- Public Key Infrastructure (PKI)
- Digital certificates
- Certificate validation

---

# Advantages of CBA

## User Experience

Benefits:
- Direct Microsoft Entra authentication
- Easy certificate mapping
- Flexible authentication policies

---

# Administration Benefits

Advantages:
- No AD FS dependency
- Simplified deployment
- Cloud-native authentication

---

# Security Benefits

Benefits:
- No cloud-stored passwords
- Strong authentication
- Supports phishing-resistant MFA
- Integrates with Conditional Access

---

# Authentication Strength Policies

Administrators can:
- Define certificate requirements
- Configure single-factor vs multifactor rules

---

# Passwordless Authentication and Zero Trust

Passwordless authentication supports:
- Zero Trust security principles

Benefits:
- Verify every sign-in
- Minimize attack surface
- Reduce credential compromise

---

# Passwordless vs Traditional Passwords

## Traditional Passwords

Problems:
- Weak passwords
- Password reuse
- Phishing vulnerability
- Credential theft

---

# Passwordless Authentication

Advantages:
- Stronger security
- Better user experience
- Reduced password fatigue
- Better compliance

---

# Microsoft Recommendations

Microsoft recommends:
- MFA for all users
- Passwordless authentication where possible
- FIDO2 for high-security environments
- Microsoft Authenticator for mobile users
- Windows Hello for Business for enterprise Windows devices

---

# Key Takeaways

Passwordless authentication:
- Removes dependency on passwords
- Improves security posture
- Reduces phishing attacks
- Supports modern Zero Trust environments

Microsoft Entra ID supports:
- Windows Hello for Business
- Microsoft Authenticator
- FIDO2 security keys
- macOS Platform Credentials
- Smart cards
- Certificate-based authentication

