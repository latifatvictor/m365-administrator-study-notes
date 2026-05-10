# Plan for Directory Synchronization Using Microsoft Entra Cloud Sync

## Overview

Microsoft Entra Cloud Sync is a lightweight, cloud-managed directory synchronization solution.

It synchronizes identities from:

```text
On-premises Active Directory → Microsoft Entra ID
```

Cloud Sync is useful for organisations that want:

- Simple setup
- Lower infrastructure requirements
- Cloud-managed provisioning
- Multiple agent high availability
- Support for disconnected forests

---

# What Microsoft Entra Cloud Sync Synchronizes

Microsoft Entra Cloud Sync can synchronize:

- Users
- Groups
- Contacts

---

# Common Cloud Sync Topologies

Microsoft Entra Cloud Sync supports several deployment topologies.

---

# 1. Single Forest, Single Microsoft Entra Tenant

This is the simplest topology.

```text
Single AD Forest → Single Microsoft Entra Tenant
```

Best for:

- Small organisations
- Simple AD environments
- Standard hybrid identity deployments

---

# 2. Multi-Forest, Single Microsoft Entra Tenant

This topology includes multiple AD forests synchronizing to one Microsoft Entra tenant.

```text
Forest A
Forest B
Forest C
   ↓
Single Microsoft Entra Tenant
```

Best for:

- Larger organisations
- Businesses with multiple AD forests
- Complex identity environments

---

# 3. Existing Forest with Entra Connect Sync and New Forest with Cloud Sync

This scenario is used when an organisation already has Microsoft Entra Connect Sync for an existing forest but wants to onboard a new forest using Cloud Sync.

```text
Existing Forest → Entra Connect Sync → Microsoft Entra ID
New Forest      → Cloud Sync        → Microsoft Entra ID
```

Best for:

- Mergers
- Acquisitions
- Adding a new business unit
- Gradual migration to Cloud Sync

---

# 4. Piloting Cloud Sync in an Existing Hybrid AD Forest

This allows both tools to exist in the same forest during testing.

```text
Same Forest
   ├── Entra Connect Sync
   └── Entra Cloud Sync
```

Important rule:

```text
Each object must be in scope for only one synchronization tool.
```

---

# Important Topology Rules

Organisations must ensure:

- Users are uniquely identified across all forests
- Groups are uniquely identified across all forests
- A user or group is represented only once
- Objects are not synchronised by both tools
- Matching across forests does not occur with Cloud Sync

---

# Important Warning

Microsoft does not support modifying or operating Cloud Sync outside documented configurations.

Unsupported changes may cause:

- Inconsistent synchronization
- Unsupported deployment state
- Loss of Microsoft technical support

---

# Source Anchor

Cloud Sync automatically selects the source anchor.

It uses:

```text
ms-DS-ConsistencyGuid
```

if present.

If not present, it uses:

```text
ObjectGUID
```

---

# Important Source Anchor Rule

You cannot change the attribute used for the source anchor.

---

# Prerequisites for Microsoft Entra Cloud Sync

Before deploying Cloud Sync, organisations need the following prerequisites.

---

# 1. Group Managed Service Account

Cloud Sync uses a:

```text
Group Managed Service Account (gMSA)
```

to run the lightweight agent service.

---

# Benefits of gMSA

A gMSA provides:

- Automatic password management
- Simplified Service Principal Name management
- Delegated administration
- Support across multiple servers

---

# 2. Required Permissions to Create gMSA

To create the gMSA, you need:

- Domain Administrator credentials
OR
- Enterprise Administrator credentials

---

# 3. Microsoft Entra Admin Account

You need a:

```text
Hybrid Identity Administrator
```

account for the Microsoft Entra tenant.

Important:

- The account must not be a guest user

---

# 4. On-Premises Server Requirement

The Cloud Sync agent must be installed on an on-premises server running:

```text
Windows Server 2016 or later
```

---

# Server Security Requirement

The Cloud Sync agent server should be treated as:

```text
Tier 0 infrastructure
```

because it handles identity synchronization.

---

# Domain Controller Installation

Cloud Sync agent installation on a domain controller is supported.

However, organisations should still apply strong security controls.

---

# 5. High Availability Requirement

Microsoft recommends installing:

```text
Three active Cloud Sync agents
```

for high availability.

---

# Why Multiple Agents Matter

Multiple agents help Cloud Sync continue working if:

- One server fails
- One agent stops responding
- A network issue affects one agent

---

# Important Agent Behaviour

Cloud Sync supports multiple active agents.

However:

```text
Only one agent is active for a given synchronization job at a time.
```

---

# 6. Firewall Configuration

On-premises firewall rules must allow the Cloud Sync agent to communicate with Microsoft Entra ID.

Organisations should ensure required outbound connectivity is allowed.

---

# Real Work Scenario

A company acquires another organisation.

The acquired company has:

- A separate AD forest
- No direct network connectivity to the parent company
- Its own domain controllers

The parent company can deploy Microsoft Entra Cloud Sync by:

- Installing a Cloud Sync agent in the acquired company's environment
- Synchronizing users to the same Microsoft Entra tenant
- Avoiding complex network connectivity between forests

---

# Cloud Sync Deployment Checklist

Before deployment, confirm:

- Supported topology is selected
- Users are unique across forests
- Groups are unique across forests
- Objects are not duplicated across tools
- gMSA can be created
- Hybrid Identity Administrator account is available
- Cloud Sync server runs Windows Server 2016 or later
- Server is secured as Tier 0
- Firewall allows required outbound communication
- At least three agents are planned for high availability

---

# Cloud Sync vs Entra Connect Sync

| Area | Cloud Sync | Entra Connect Sync |
|---|---|---|
| Configuration location | Cloud | On-premises |
| Agent type | Lightweight | Full sync engine |
| Best for | Simple or disconnected forests | Complex hybrid scenarios |
| Infrastructure | Lower | Higher |
| Management | Cloud-managed | Server-managed |
| Advanced features | Fewer | More |

---

# When to Choose Cloud Sync

Choose Cloud Sync when:

- You want a lightweight solution
- You want cloud-managed provisioning
- You have disconnected forests
- You want faster setup
- You want lower maintenance
- You are onboarding a new forest
- You are piloting a modern sync approach

---

# When Not to Choose Cloud Sync

Cloud Sync may not be ideal if you need:

- Advanced attribute customization
- Device writeback
- Exchange hybrid writeback
- Pass-through authentication
- Complex synchronization rules

In those cases, Microsoft Entra Connect Sync may be more suitable.

---

# Common Mistakes to Avoid

- Synchronizing the same object with both tools
- Assuming Cloud Sync performs cross-forest matching
- Using duplicate users across forests
- Ignoring source anchor behaviour
- Using unsupported configurations
- Installing too few agents
- Treating the agent server as low-security infrastructure

---

# Important Exam Points

- Cloud Sync uses lightweight agents
- Cloud Sync is managed from the cloud
- It supports single forest and multi-forest topologies
- It supports disconnected forests
- Matching across forests does not occur
- Each user or group should be represented only once
- Each object must be in scope for only one sync tool
- Source anchor is automatically selected
- Source anchor cannot be changed
- Cloud Sync uses a gMSA
- Hybrid Identity Administrator account is required
- Agent server requires Windows Server 2016 or later
- Microsoft recommends three active agents for high availability

---

# Common Interview Questions

## Q1: What is Microsoft Entra Cloud Sync?

A lightweight cloud-managed directory synchronization tool that synchronizes on-premises AD objects to Microsoft Entra ID.

---

## Q2: What account does Cloud Sync use to run the agent service?

A group Managed Service Account, also called gMSA.

---

## Q3: What server version is required for the Cloud Sync agent?

Windows Server 2016 or later.

---

## Q4: How many Cloud Sync agents does Microsoft recommend for high availability?

Three active agents.

---

## Q5: Does Cloud Sync support disconnected forests?

Yes.

---

## Q6: Does Cloud Sync perform matching across forests?

No.

---

## Q7: What happens if the same object is in scope for both Cloud Sync and Entra Connect Sync?

This should be avoided because each object must be managed by only one synchronization tool.

---

## Q8: What source anchor does Cloud Sync use?

It uses ms-DS-ConsistencyGuid if present. Otherwise, it uses ObjectGUID.

---

# Summary

Microsoft Entra Cloud Sync is a modern, lightweight synchronization tool for hybrid identity.

It is best suited for:

- Simpler environments
- Disconnected forests
- Mergers and acquisitions
- Lower maintenance deployments
- Cloud-managed provisioning

Key planning points include:

- Choose a supported topology
- Ensure users and groups are unique
- Avoid duplicate synchronization scope
- Prepare gMSA permissions
- Use a Hybrid Identity Administrator account
- Deploy Windows Server 2016 or later
- Install multiple agents for high availability
- Follow only supported Microsoft configurations
