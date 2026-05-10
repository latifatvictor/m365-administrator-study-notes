# Prepare for Directory Synchronization

## Overview

Directory synchronization helps organisations use one identity across both on-premises and cloud applications.

In Microsoft 365, this usually means synchronising identities from:

- On-premises Active Directory Domain Services (AD DS)
- Microsoft Entra ID

This allows users to access on-premises and cloud resources with a consistent identity.

---

# What Is Provisioning?

Provisioning is the process of:

- Creating an object
- Keeping the object updated
- Deleting the object when it is no longer needed

---

# Provisioning Example

When a new employee joins:

1. HR creates the employee record.
2. A user account is created in Active Directory.
3. The account is synchronised to Microsoft Entra ID.
4. Licences and application access are assigned.
5. The user can access the systems they need from day one.

---

# Types of Provisioning

| Provisioning Type | Description |
|---|---|
| HR provisioning | User starts from HR system |
| Directory provisioning | User is created or synchronised in AD DS or Entra ID |
| App provisioning | User is given access to required applications |

---

# On-Premises Identity Provisioning

On-premises identity provisioning usually means provisioning users from Active Directory into Microsoft Entra ID.

This is done using:

- Microsoft Entra Connect Sync
- Microsoft Entra Cloud Sync

---

# Key Preparation Areas

Before enabling directory synchronization, organisations should review:

- On-premises Active Directory preparation
- UPN suffixes
- Microsoft 365 IdFix tool

---

# Important Long-Term Commitment

After directory synchronization is enabled, synchronised objects must usually be edited using on-premises Active Directory tools.

This means:

- AD DS becomes the source of authority
- Most user identity changes happen on-premises
- Changes then synchronise to Microsoft Entra ID

---

# On-Premises Active Directory Preparation

Before directory synchronization, organisations should prepare AD DS by completing three key tasks:

1. Identify the source of authority
2. Clean up Active Directory
3. Set up auditing

---

# Source of Authority

Source of authority means the original location where an identity object is mastered.

For hybrid identity, this is usually:

```text
On-premises Active Directory
```

After synchronisation, the source of authority transfers from Microsoft 365 to the on-premises directory.

---

# What This Means in Real Life

If a user is synchronised from AD DS:

- You cannot fully manage that user directly in Microsoft 365
- You must update the user in Active Directory
- The update then syncs to Microsoft Entra ID

---

# Active Directory Cleanup

Before synchronisation, organisations should clean up AD DS to prevent sync errors.

---

# Common Cleanup Tasks

- Remove duplicate proxyAddresses
- Remove duplicate userPrincipalName values
- Update blank UPN attributes
- Fix invalid UPN attributes
- Remove invalid characters from user attributes

---

# Attributes to Review

| Attribute | Purpose |
|---|---|
| givenName | First name |
| surname / sn | Last name |
| sAMAccountName | Legacy logon name |
| displayName | Display name |
| mail | Email address |
| proxyAddresses | Email aliases |
| mailNickname | Exchange alias |
| userPrincipalName | Sign-in name |

---

# Why Cleanup Matters

Poor Active Directory data can cause:

- Synchronisation failures
- Duplicate user accounts
- Incorrect sign-in names
- Licensing issues
- Mail flow issues
- User confusion

---

# Real Work Scenario

A user has two accounts with the same proxyAddress.

When synchronisation runs:

- Microsoft Entra ID detects a duplicate
- One or both objects may fail to sync
- The user may not appear correctly in Microsoft 365

Fix:

- Remove the duplicate proxyAddress in AD DS
- Run synchronization again

---

# UPN Suffixes

UPN stands for User Principal Name.

Example:

```text
latifat@contoso.com
```

The UPN suffix is the part after the @ symbol.

Example:

```text
@contoso.com
```

---

# UPN Requirements

Before directory synchronization, verify that:

- Each user has a UPN suffix
- The suffix is correct
- The suffix is routable on the internet
- The suffix matches a verified Microsoft 365 domain

---

# Best Practice

Microsoft recommends using the user’s primary SMTP email address as their UPN.

Example:

```text
Email: latifat@contoso.com
UPN:   latifat@contoso.com
```

---

# Why Use Email Address as UPN?

It reduces confusion because users often expect to sign in with their email address.

This is especially useful for:

- Microsoft Teams
- Outlook
- Skype for Business
- Microsoft 365 apps

---

# Non-Routable UPN Problem

If the on-premises UPN uses a non-routable domain such as:

```text
latifat@contoso.local
```

Microsoft 365 may use the default tenant domain instead:

```text
latifat@contoso.onmicrosoft.com
```

This can confuse users and cause sign-in issues.

---

# Recommended UPN Format

Use:

```text
user@verifieddomain.com
```

Avoid:

```text
user@domain.local
user@internal.local
user@company.private
```

---

# UPN Mismatch Scenario

A user is licensed in Microsoft 365 before the custom domain is verified.

Result:

- Microsoft 365 UPN may not match on-premises UPN
- User sign-in name may be inconsistent

Fix:

- Verify the custom domain
- Update the user’s UPN
- Ensure cloud and on-premises identity values align

---

# Important Warning

Before changing UPN suffixes in AD DS, check whether any applications depend on the existing UPN.

Some legacy applications may break if UPNs are changed without planning.

---

# Microsoft 365 IdFix Tool

The IdFix tool helps identify and fix directory errors before synchronization.

It is used to prepare Active Directory for Microsoft 365 directory synchronization.

---

# What IdFix Does

IdFix checks AD DS for common sync issues such as:

- Duplicate values
- Invalid characters
- Blank attributes
- Formatting problems
- Problematic object attributes

---

# Why Use IdFix?

IdFix helps organisations:

- Prevent sync failures
- Clean directory data
- Identify problematic users
- Fix issues before deployment
- Improve directory synchronization success

---

# How IdFix Works

IdFix:

1. Queries Active Directory
2. Detects potential sync errors
3. Displays errors in a grid
4. Allows administrators to review issues
5. Applies selected fixes only

---

# IdFix Features

| Feature | Description |
|---|---|
| Error detection | Finds sync-related attribute problems |
| Manual review | Admin chooses what to fix |
| Transaction rollback | Can undo confirmed updates |
| Exclusions | Protects critical system objects |
| Export | Saves results to CSV or LDF |
| Import CSV | Allows offline editing |
| Verbose logging | Records changes |
| Multi-tenant support | Supports different Microsoft 365 tenant types |

---

# Important IdFix Warning

Use IdFix carefully because it can bulk-update Active Directory objects.

Always:

- Review changes before applying
- Export results first
- Test in a controlled way
- Have a rollback plan

---

# Real Work Scenario

Before deploying Microsoft Entra Connect Sync, an administrator runs IdFix.

IdFix finds:

- Duplicate proxyAddresses
- Blank UPNs
- Invalid characters in displayName

The administrator:

- Reviews the list
- Fixes selected objects
- Exports a report
- Runs IdFix again to confirm cleanup

Result:

- Fewer synchronization errors
- Cleaner Microsoft 365 onboarding

---

# Directory Synchronization Readiness Checklist

Before enabling directory synchronization, confirm:

- AD DS is healthy
- Source of authority is understood
- Duplicate attributes are cleaned
- UPN suffixes are correct
- Custom domain is verified in Microsoft 365
- IdFix has been run
- Users have valid UPNs
- Attributes are clean
- Auditing is enabled
- Applications affected by UPN changes are reviewed

---

# Common Directory Sync Issues

| Issue | Cause |
|---|---|
| User fails to sync | Invalid attribute |
| Duplicate object error | Duplicate proxyAddress or UPN |
| Wrong sign-in name | Incorrect UPN suffix |
| User cannot access services | No licence assigned |
| Cloud object cannot be edited | Object is mastered on-premises |

---

# Real Interview Scenario

Question:

A user synced from on-premises AD DS needs their display name changed. Where should you change it?

Answer:

Change it in on-premises Active Directory because AD DS is the source of authority for synchronised objects.

---

# Best Practices

- Clean Active Directory before synchronisation
- Use routable UPN suffixes
- Match UPN to primary SMTP address
- Run IdFix before deployment
- Verify custom domains before licensing users
- Document source of authority
- Enable auditing
- Review applications before UPN changes
- Treat directory sync as a long-term commitment

---

# Common Interview Questions

## Q1: What is provisioning?

Provisioning is creating, updating, and deleting identity objects based on business conditions.

---

## Q2: What is directory synchronization?

The process of synchronising directory objects between on-premises AD DS and Microsoft Entra ID.

---

## Q3: What is source of authority?

The location where an identity object is mastered and managed.

---

## Q4: After synchronization, where should synced users be edited?

In on-premises Active Directory.

---

## Q5: What is a UPN suffix?

The part of the user principal name after the @ symbol.

Example:

```text
@contoso.com
```

---

## Q6: What is Microsoft’s UPN best practice?

Use the user’s primary SMTP email address as their UPN.

---

## Q7: What is the IdFix tool used for?

It identifies and fixes Active Directory object errors before synchronization.

---

## Q8: Why should you avoid non-routable UPN suffixes?

They can cause Microsoft 365 to use the onmicrosoft.com domain, which may confuse users and cause sign-in issues.

---

# Key Exam Points

- Provisioning creates, updates, and deletes identity objects
- Directory synchronization connects AD DS with Microsoft Entra ID
- Microsoft Entra Connect Sync and Cloud Sync are used for synchronisation
- Directory synchronization is a long-term commitment
- Synced objects are managed from on-premises AD DS
- AD DS becomes the source of authority
- Active Directory cleanup is required before sync
- Duplicate proxyAddresses and UPNs cause sync errors
- UPN suffix should be internet-routable
- Primary SMTP address should usually match UPN
- IdFix identifies and fixes common sync errors
- IdFix should be used carefully because it can bulk update AD objects

---

# Summary

Preparing for directory synchronization is a critical step in Microsoft 365 hybrid identity deployment.

Before enabling synchronization, organisations should:

- Clean up Active Directory
- Confirm the source of authority
- Review UPN suffixes
- Use routable domains
- Run the Microsoft 365 IdFix tool
- Plan for long-term on-premises management

A clean and well-prepared directory reduces synchronization errors and improves the Microsoft 365 user experience.
