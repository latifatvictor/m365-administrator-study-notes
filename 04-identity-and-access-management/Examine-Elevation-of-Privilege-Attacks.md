# Examine Elevation of Privilege Attacks

## Overview

An elevation of privilege attack occurs when attackers increase their level of access after compromising one or more user accounts. Elevation of privilege attacks occur when attackers gain higher permissions after compromising accounts. The most effective defenses include Microsoft Entra MFA, minimizing Global Administrator accounts, continuous monitoring, auditing, and strict privilege management.

Attackers commonly attempt to:
- Gain administrator privileges
- Access sensitive systems
- Control cloud environments
- Manipulate tenant configurations
- Create hidden privileged accounts

In Microsoft 365 environments, attackers frequently target:

- Global Administrator privileges
- Service administrator roles
- Sensitive workloads and data

---

# What is Elevation of Privilege?

Elevation of privilege refers to:
- Attackers gaining higher permissions than originally granted.

For example:
- A compromised standard user account becomes a Global Administrator account.

---

# Common Goals of Attackers

Attackers typically attempt to:

- Gain Global Administrator access
- Access sensitive mailboxes
- Disable security protections
- Create persistence mechanisms
- Move laterally across systems
- Steal sensitive data

---

# Global Administrator Privileges

Global Administrator is one of the most powerful roles in Microsoft 365.

With Global Administrator access, attackers can:

- Manage users
- Reset passwords
- Change tenant settings
- Access security configurations
- Grant permissions
- Create new accounts
- Delete resources

---

# Creating Hidden Administrator Accounts

A common attacker tactic is:

1. Create a new account.
2. Assign Global Administrator privileges.
3. Use the account secretly.

This tactic allows attackers to:
- "Hide in plain sight."

Organizations may overlook these accounts if they don't regularly review administrator accounts.

---

# Persistence Techniques

Attackers often attempt to maintain long-term access by:

- Creating hidden accounts
- Modifying permissions
- Configuring mailbox forwarding
- Changing transport rules
- Adding delegate permissions

---

# Risks of Elevation of Privilege

Elevation of privilege attacks can lead to:

- Full tenant compromise
- Data theft
- Email interception
- Unauthorized access
- Security configuration changes
- Service disruption

---

# Preventing Elevation of Privilege Attacks

Organizations should implement layered security protections.

---

# Microsoft Entra Multifactor Authentication (MFA)

Microsoft recommends implementing:

```text
Microsoft Entra Multifactor Authentication (MFA)
