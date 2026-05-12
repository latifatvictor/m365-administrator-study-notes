# Configure Microsoft Entra Connect Sync

## Overview

Microsoft Entra Connect Sync is installed using a setup wizard.

Always download the latest version before installation because Microsoft cloud services are continuously updated.

The installation wizard offers two setup modes:

- Express setup
- Custom setup

---

# Express Setup

## What It Is

Express setup is the default setup option.

It is designed for the most common deployment scenario:

```text
Single forest + Password Hash Synchronisation
```

---

# When to Use Express Setup

Use Express setup when the organisation has:

- One Active Directory forest
- Standard synchronisation needs
- No advanced filtering requirements
- No complex hybrid identity requirements
- A preference for quick deployment

---

# What Express Setup Enables

Express setup enables:

```text
Password Hash Synchronisation (PHS)
```

This allows users to sign in to Microsoft 365 using the same password they use on-premises.

---

# Benefits of Express Setup

- Simple to install
- Uses Microsoft recommended defaults
- Reduces manual configuration
- Enables password hash synchronisation
- Supports seamless directory synchronisation
- Helps keep cloud identities up to date
- Enables automatic upgrade
- Suitable for most basic hybrid identity deployments

---

# What Express Setup Configures

During Express setup, the installer will:

- Install the synchronisation engine
- Configure Microsoft Entra Connect Sync
- Configure the on-premises Active Directory connector
- Enable Password Hash Synchronisation
- Configure synchronisation services
- Optionally configure Exchange hybrid synchronisation services
- Enable automatic upgrade

---

# Optional Final Step

At the end of installation, you can choose to start synchronisation immediately.

---

# Real Work Scenario

A company has:

- One AD forest
- One Microsoft 365 tenant
- No Exchange hybrid
- No custom filtering

Best setup choice:

```text
Express setup
```

---

# Custom Setup

## What It Is

Custom setup gives more control over the Microsoft Entra Connect Sync installation.

Use it when Express setup does not meet the organisation’s requirements.

---

# When to Use Custom Setup

Use Custom setup when the organisation has:

- Multiple forests
- Custom filtering requirements
- Pass-through Authentication requirements
- AD FS federation
- Non-Microsoft identity provider
- Password writeback requirement
- Device writeback requirement
- Group writeback requirement
- Exchange hybrid deployment
- Existing SQL Server
- Custom service account requirement

---

# Custom Setup Optional Components

## Custom Installation Location

Allows you to install Microsoft Entra Connect Sync in a different location.

---

## Existing SQL Server

Allows you to use an existing SQL Server instead of the default local SQL option.

Useful for larger or more controlled environments.

---

## Existing Service Account

Allows you to use a known service account.

Important when using a remote SQL Server.

---

## Custom Sync Groups

Allows you to specify your own local management groups.

By default, Microsoft Entra Connect creates groups such as:

- Administrators
- Operators
- Browse
- Password Reset

Important:

```text
Custom sync groups must be local to the server, not domain groups.
```

---

# Custom Setup Features

| Feature | What It Does | When to Use |
|---|---|---|
| Select SSO method | Choose PHS, PTA, AD FS, or no SSO | When planning authentication |
| Connect multiple forests | Connect more than one AD forest | Multi-forest environments |
| Matching across forests | Controls how users are represented across forests | Multi-forest identity matching |
| OU filtering | Synchronise only selected OUs | Pilot or controlled rollout |
| Source anchor | Links on-premises user to cloud user | Identity matching scenarios |
| Sign-in attribute | Choose UPN or Alternate ID | When UPN is non-routable |
| Exchange hybrid | Supports Exchange coexistence | Exchange on-prem to Exchange Online |
| Mail public folders | Sync mail-enabled public folders | Exchange public folder scenarios |
| App and attribute filtering | Sync only selected attributes | App-specific sync requirements |
| Password writeback | Writes cloud password changes back to AD | Self-service password reset |
| Group writeback | Writes Microsoft 365 groups back to AD | Exchange hybrid scenarios |
| Device writeback | Writes cloud device objects back to AD | Conditional Access scenarios |
| Directory extension sync | Syncs custom AD attributes | Custom schema requirements |

---

# Password Hash Synchronisation Only

Password Hash Synchronisation is the default option used by Express setup.

Organisations may choose PHS only when they want:

- Simpler deployment
- Less infrastructure
- On-premises password policy control
- Fewer authentication components
- Reduced password fatigue for users

---

# SSO with PHS and PTA

If SSO is enabled during Custom setup, Microsoft Entra Connect Sync can configure:

- Password Hash Synchronisation
- Pass-through Authentication

---

# Benefits of SSO with PHS and PTA

- Users sign in with on-premises credentials
- Better sign-in experience
- Fewer password prompts
- No separate cloud password needed
- PTA validates credentials against on-premises AD
- PHS can help provide fallback during on-premises issues
- Supports hybrid access to cloud and on-premises resources

---

# AD FS Federation

If the organisation already uses AD FS, Custom setup can configure federation.

The wizard may ask for:

- AD FS farm name
- Service account
- TLS/SSL certificate
- Federation information

---

# Staging Mode

Custom setup can enable:

```text
Staging mode
```

Staging mode allows a second Microsoft Entra Connect Sync server to run in parallel without exporting changes to Microsoft Entra ID.

---

# What Staging Mode Does

A staging server:

- Imports data
- Synchronises internally
- Does not export to Microsoft Entra ID
- Does not run Password Hash Synchronisation
- Does not run Password Writeback

until promoted.

---

# When to Use Staging Mode

Use staging mode for:

- Backup sync server
- Disaster recovery
- Migration
- Testing changes
- Safe upgrades

---

# Real Work Scenario

A company wants to replace its current Microsoft Entra Connect Sync server.

They:

1. Install a new server using Custom setup.
2. Enable staging mode.
3. Validate configuration.
4. Promote the staging server.
5. Retire the old active server.

---

# Express vs Custom Setup

| Area | Express Setup | Custom Setup |
|---|---|---|
| Best for | Simple deployments | Advanced deployments |
| Forests | Single forest | Multiple forests |
| Default auth | PHS | PHS, PTA, AD FS |
| Filtering | Basic/default | OU, domain, attribute filtering |
| SQL choice | Default local SQL | Existing SQL supported |
| Service account | Auto-created | Custom account supported |
| Writeback | Limited | Password, device, group writeback |
| Staging mode | No | Yes |
| Control level | Low | High |

---

# Common Mistakes to Avoid

- Using Express setup for multi-forest environments
- Forgetting to plan authentication method
- Enabling writeback without understanding impact
- Synchronising too many unnecessary OUs
- Not planning source anchor carefully
- Using non-routable UPNs without Alternate ID planning
- Forgetting staging mode for migration or disaster recovery

---

# Important Exam Points

- Express setup is the default option
- Express setup is for single forest deployments
- Express setup enables Password Hash Synchronisation
- Custom setup supports multiple forests
- Custom setup supports PTA, AD FS, filtering, and writeback
- Source anchor links on-premises and cloud identities
- Alternate ID can be used when UPN is not routable
- Password writeback supports cloud password changes writing back to AD
- Staging mode does not export changes until promoted
- Only one active sync server is supported per tenant

---

# Common Interview Questions

## Q1: What are the two Microsoft Entra Connect Sync setup options?

Express setup and Custom setup.

---

## Q2: What does Express setup enable by default?

Password Hash Synchronisation.

---

## Q3: When should Custom setup be used?

When the organisation needs multiple forests, filtering, AD FS, PTA, writeback, custom SQL, custom service accounts, or staging mode.

---

## Q4: What is the source anchor?

The unique attribute that links an on-premises identity to its Microsoft Entra ID cloud identity.

---

## Q5: What is Alternate ID?

An alternative sign-in attribute, such as email, used when UPN is not suitable.

---

## Q6: What is password writeback?

A feature that writes password changes from Microsoft Entra ID back to on-premises Active Directory.

---

## Q7: What is staging mode?

A passive Microsoft Entra Connect Sync server mode used for testing, migration, disaster recovery, or backup.

---

## Q8: Does staging mode export changes to Microsoft Entra ID?

No.

---

# Summary

Microsoft Entra Connect Sync can be installed using Express or Custom setup.

Express setup is best for simple single-forest environments and enables Password Hash Synchronisation by default.

Custom setup is best for complex environments that need:

- Multiple forests
- Authentication choices
- Filtering
- Writeback
- Exchange hybrid
- Custom SQL
- Staging mode

Choosing the correct setup mode is important for a stable, secure, and scalable hybrid identity deployment.
