# Troubleshoot Directory Synchronization

## Overview

Microsoft 365 administrators must troubleshoot any directory synchronization issues that occur between on-premises Active Directory and Microsoft Entra ID. Troubleshooting directory synchronization involves monitoring synchronization health, resolving duplicate attribute conflicts, reviewing synchronization operations, managing password synchronization, and ensuring connectivity between on-premises Active Directory and Microsoft Entra ID. Microsoft provides tools such as Synchronization Service Manager, Microsoft Entra Connect Health, PowerShell cmdlets, and the Directory Synchronization Troubleshooter to help administrators diagnose and resolve synchronization problems efficiently.

Administrators typically:
- Analyze logs
- Review synchronization status
- Resolve synchronization errors
- Monitor synchronization health

Organizations can use:
- Microsoft Entra Connect Sync
- Microsoft Entra Cloud Sync

to synchronize identities.

---

# Common Directory Synchronization Issues

Typical synchronization problems include:

- Authentication errors
- Incorrect credentials
- Disabled synchronization
- Active Directory changes
- Corrupted Active Directory
- Duplicate attributes
- Filtering issues
- Connectivity problems

---

# Examples of Synchronization Problems

Examples include:

- Incorrect on-premises credentials
- Incorrect Microsoft 365 credentials
- Disabled directory synchronization
- OU scoping changes
- Attribute filtering issues
- Duplicate UserPrincipalName (UPN)
- Duplicate ProxyAddress values

---

# Key Troubleshooting Tools and Tasks

Microsoft 365 administrators should understand:

- Deactivating and reactivating synchronization
- Viewing synchronization errors
- Duplicate attribute resiliency
- Synchronization notifications
- Directory Synchronization Troubleshooter
- Synchronization Service Manager
- Password hash synchronization troubleshooting

---

# Deactivate and Reactivate Directory Synchronization

When directory synchronization is:
- Disabled

the source of authority changes from:
- On-premises Active Directory

to:
- Microsoft 365

---

# Source of Authority

## With Directory Synchronization Enabled
Source of authority:
- On-premises Active Directory

## With Directory Synchronization Disabled
Source of authority:
- Microsoft 365

---

# Important Warning

When directory synchronization is re-enabled:

- Microsoft Entra Connect overwrites cloud object changes
- Microsoft 365 changes can be lost

---

# Example Scenario

1. Contoso enables directory synchronization.
2. Users are created on-premises.
3. Users synchronize to Microsoft 365.
4. Contoso disables synchronization.
5. Administrators edit users directly in Microsoft 365.
6. Contoso re-enables synchronization.
7. On-premises objects overwrite cloud changes.

---

# Duplicate Attribute Resiliency

Microsoft Entra ID includes:
- Duplicate attribute resiliency

This feature handles:
- Duplicate UPN conflicts
- Duplicate ProxyAddress conflicts

---

# Uniqueness Requirements

The following attributes must be unique:

- UserPrincipalName (UPN)
- ProxyAddress

across:
- Users
- Groups
- Contacts

within:
- A Microsoft Entra tenant

---

# What Happens During Duplicate Conflicts

Without duplicate resiliency:
- Object creation fails
- Object updates fail
- Sync retries continuously

With duplicate resiliency:
- Conflicting attributes are quarantined
- Synchronization continues

---

# Placeholder UPN Format

Microsoft Entra ID assigns temporary placeholder values using this format:

```text
<OriginalPrefix>+<4DigitNumber>@<Tenant>.onmicrosoft.com
