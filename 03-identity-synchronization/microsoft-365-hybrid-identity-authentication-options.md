File Name: microsoft-365-hybrid-identity-authentication-options.md

# Microsoft 365 Hybrid Identity Authentication Options

## Overview

Hybrid identity allows organisations to synchronise on-premises Active Directory Domain Services (AD DS) identities with Microsoft Entra ID.

This lets users access Microsoft 365 cloud services using identities that originate from on-premises AD DS.

---

# Important Note

Azure Active Directory (Azure AD) is now called Microsoft Entra ID.

---

# Key Point

When AD DS users are synchronised to Microsoft Entra ID for the first time:

- They do not automatically receive Microsoft 365 licences
- They cannot access Microsoft 365 services until licensed
- A usage location must be assigned first
- Licences can be assigned manually or through group-based licensing

---

# Hybrid Identity Authentication Options

There are two main authentication types:

1. Managed authentication
2. Federated authentication

---

# Authentication Options Summary

| Authentication Type | Description |
|---|---|
| Managed authentication | Microsoft Entra ID handles authentication |
| Federated authentication | Microsoft Entra ID redirects authentication to another identity provider |

---

# Managed Authentication

Managed authentication means Microsoft Entra ID is responsible for handling the sign-in process.

There are two managed authentication methods:

1. Password Hash Synchronisation (PHS)
2. Pass-through Authentication (PTA)

---

# Password Hash Synchronisation (PHS)

## What It Is

Password Hash Synchronisation allows users to use the same username and password for:

- On-premises resources
- Microsoft 365 cloud services

Microsoft Entra ID performs the authentication using a synchronised password hash.

---

# How PHS Works

```text
User signs in
   ↓
Microsoft Entra ID checks synchronised password hash
   ↓
Authentication succeeds or fails
   ↓
User accesses Microsoft 365
```

---

# Important Security Point

PHS does not send or store the user's actual password in Microsoft Entra ID.

Only a protected hash of the password hash is synchronised.

---

# Benefits of PHS

- Simple to deploy
- No additional authentication infrastructure required
- Users keep the same password for cloud and on-premises access
- Reduces password fatigue
- Supports cloud authentication
- Helps with Microsoft Entra ID protection features

---

# Best Use Case for PHS

PHS is best for organisations that want:

- Simple hybrid identity
- Cloud-based authentication
- Lower infrastructure complexity
- High availability

---

# Pass-through Authentication (PTA)

## What It Is

Pass-through Authentication validates user passwords directly against on-premises AD DS using lightweight authentication agents.

Microsoft Entra ID does not store password hashes for authentication.

---

# How PTA Works

```text
User signs in
   ↓
Microsoft Entra ID receives request
   ↓
PTA agent sends validation to on-premises AD DS
   ↓
AD DS validates credentials
   ↓
Result returned to Microsoft Entra ID
   ↓
User accesses Microsoft 365
```

---

# Important Security Point

PTA does not store or send passwords to Microsoft 365.

Passwords are validated against on-premises AD DS.

---

# Benefits of PTA

- Uses on-premises passwords for cloud services
- Enforces on-premises account policies immediately
- Supports stronger security and compliance requirements
- Reduces the number of passwords users must remember

---

# PTA Supports

- Password-based authentication
- Smart card authentication
- Some multifactor authentication scenarios
- Custom authentication ports
- Failover configuration

---

# Best Use Case for PTA

PTA is best for organisations that need:

- Immediate enforcement of on-premises account status
- On-premises password policy control
- Sign-in hour enforcement
- Authentication directly against AD DS

---

# PTA Consideration

PTA requires organisations to install and maintain lightweight on-premises agents.

This may not suit every organisation.

---

# PHS vs PTA

| Feature | PHS | PTA |
|---|---|---|
| Authentication location | Microsoft Entra ID | On-premises AD DS |
| Password hash stored in Entra ID | Yes, securely hashed | No |
| Extra agent required | No | Yes |
| Simpler deployment | Yes | Moderate |
| Immediate on-premises policy enforcement | Limited | Yes |
| Best for | Simplicity and resilience | Strong on-premises control |

---

# Federated Authentication

## What It Is

Federated authentication redirects the authentication process to a trusted identity provider.

The identity provider validates the user's sign-in.

---

# Common Federation Providers

- Active Directory Federation Services (AD FS)
- PingFederate
- Okta
- Other SAML or WS-Federation compatible providers

---

# How Federated Authentication Works

```text
User signs in to Microsoft 365
   ↓
Microsoft Entra ID redirects authentication
   ↓
Identity provider validates credentials
   ↓
Security token is issued
   ↓
Microsoft 365 grants access
```

---

# AD FS

Active Directory Federation Services provides:

- Single sign-on
- Identity federation
- On-premises authentication
- Support for SAML and federation protocols

---

# Benefits of Federated Authentication

- Supports complex enterprise authentication needs
- Enables single sign-on
- Uses on-premises Active Directory for authentication
- Supports MFA and Conditional Access scenarios
- Supports third-party identity providers

---

# Best Use Case for Federated Authentication

Federation is best for large enterprises with:

- Complex authentication requirements
- Existing AD FS infrastructure
- Third-party identity provider requirements
- Special sign-in needs

---

# Original Federation Proxy Model

In older federation designs:

- A federation proxy server sat between the user and AD FS
- It redirected users to the identity provider
- It helped protect credentials
- It supported load balancing and failover

---

# Web Application Proxy (WAP)

Web Application Proxy replaced the older federation proxy role from Windows Server 2012 R2 onwards.

In AD FS environments, WAP acts as:

- AD FS federation server proxy
- Reverse proxy for internal web applications

---

# Benefits of Web Application Proxy

- Supports modern authentication protocols
- Supports OAuth and OpenID Connect
- Improves application publishing
- Supports preauthentication
- Supports pass-through authentication
- Improves scalability and performance
- Integrates with Microsoft Entra ID

---

# Third-Party Identity Providers

Microsoft 365 can federate with third-party identity providers that support:

- SAML
- WS-Federation
- OpenID Connect, depending on configuration

Examples include:

- Okta
- PingFederate
- Other compatible identity platforms

---

# Administration in Hybrid Identity

Because the authoritative identities are stored in on-premises AD DS:

- Most identity management happens on-premises
- Changes are synchronised to Microsoft Entra ID
- Synchronized users cannot usually be fully managed directly in Microsoft 365 admin center

---

# Important Admin Point

For synchronised accounts, administrators usually manage core identity attributes in:

- Active Directory Users and Computers
- On-premises AD DS tools
- Hybrid identity tools

Not directly in Microsoft 365 admin center.

---

# Real Work Scenario

A company uses on-premises Active Directory and wants users to access Microsoft 365 with the same password.

Option 1:

Use PHS if the company wants simple cloud authentication with fewer moving parts.

Option 2:

Use PTA if the company needs passwords validated directly against on-premises AD DS.

Option 3:

Use federation if the company has complex SSO or third-party identity provider requirements.

---

# Common Interview Questions

## Q1: What are the two main authentication types in hybrid identity?

- Managed authentication
- Federated authentication

---

## Q2: What are the two managed authentication methods?

- Password Hash Synchronisation
- Pass-through Authentication

---

## Q3: What is Password Hash Synchronisation?

A method where password hashes are synchronised to Microsoft Entra ID so users can authenticate in the cloud using the same password.

---

## Q4: Does PHS store actual passwords in Microsoft Entra ID?

No.

It stores a protected hash, not the actual password.

---

## Q5: What is Pass-through Authentication?

A method where Microsoft Entra ID validates user credentials against on-premises AD DS using a lightweight agent.

---

## Q6: What is federated authentication?

A method where Microsoft Entra ID redirects authentication to a trusted identity provider such as AD FS or a third-party provider.

---

## Q7: What replaced the old federation proxy server?

Web Application Proxy.

---

## Q8: Why might an organisation choose PTA over PHS?

To immediately enforce on-premises account states, password policies, and sign-in restrictions.

---

# Key Exam Points

- Hybrid identity synchronises AD DS identities to Microsoft Entra ID
- Synchronised users still need usage location and licensing
- Managed authentication includes PHS and PTA
- PHS authenticates in Microsoft Entra ID
- PTA validates passwords against on-premises AD DS
- Federated authentication redirects sign-in to another identity provider
- AD FS supports SSO and federation
- Web Application Proxy replaces the older federation proxy role
- Synchronized identities are mainly managed on-premises
- PHS is simpler, PTA gives stronger on-premises control, federation supports complex authentication

---

# Summary

Hybrid identity allows organisations to connect on-premises AD DS identities with Microsoft Entra ID.

The main authentication options are:

1. Password Hash Synchronisation
2. Pass-through Authentication
3. Federated Authentication

PHS is simple and cloud-based.

PTA validates passwords directly against on-premises AD DS.

Federation redirects authentication to AD FS or another trusted identity provider.

Choosing the right method depends on the organisation's security, compliance, infrastructure, and user experience requirements.
