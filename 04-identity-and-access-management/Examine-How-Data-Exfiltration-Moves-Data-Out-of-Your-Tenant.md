# Examine How Data Exfiltration Moves Data Out of Your Tenant

## Overview

Data exfiltration is the unauthorized retrieval, transfer, or theft of data from a computer, application, or cloud service.

Once attackers compromise an organization's environment, they often attempt to move sensitive information out of the Microsoft 365 tenant.

---

# What is Data Exfiltration?

Data exfiltration refers to:
- Unauthorized movement of data outside an organization's control.

Attackers may steal:
- Emails
- Documents
- Customer records
- Financial information
- Intellectual property
- User credentials
- Directory information

---

# Common Methods of Data Exfiltration

Attackers commonly exfiltrate data through:

- Compromised user accounts
- Administrator account breaches
- Malware infections
- Privilege escalation
- External sharing
- Email forwarding
- Cloud storage uploads

---

# Account Breaches and Data Theft

One of the most common causes of data exfiltration is:
- A compromised user account.

If attackers gain access to an account with sensitive permissions, they can:
- Download files
- Read emails
- Access SharePoint data
- Steal confidential information

---

# Infrastructure-Based Attacks

Attackers may also target:

- Servers
- Endpoints
- Administrative systems

to gain:
- Local administrator access
- System-level privileges

This access allows attackers to extract sensitive data directly.

---

# Why Attackers Steal Data

Attackers are motivated by several goals, including:

- Financial gain
- Extortion
- Blackmail
- Competitive advantage
- Espionage
- Selling data on the dark web

---

# Intellectual Property Theft

Attackers often target:

- Proprietary research
- Product designs
- Business strategies
- Confidential documents

Stealing intellectual property can:
- Damage competitive advantage
- Cause financial losses

---

# Blackmail and Extortion

Attackers may threaten to:
- Leak sensitive data publicly
- Sell confidential information
- Expose private communications

unless organizations:
- Pay ransom demands

---

# Data Sold on the Black Market

Stolen data can be sold on underground markets, including:

- Personal information
- Financial records
- Login credentials
- Company secrets

---

# Types of Valuable Data

Attackers target many forms of organizational data, including:

- Emails
- Documents
- Instant messaging conversations
- Yammer discussions
- Directory information
- Financial records
- Customer data

---

# Challenges of Data Protection

Protecting data is difficult because:

- Data exists in many locations
- Users share information frequently
- Cloud collaboration increases exposure
- Sensitive information moves constantly

---

# Preventing Data Exfiltration

Organizations should implement multiple layers of protection to reduce the risk of data theft.

---

# Protect Accounts First

The first step in protecting data is:
- Preventing account breaches and privilege escalation attacks.

Organizations should secure:
- User accounts
- Administrator accounts
- Service accounts

---

# Access Control Lists (ACLs)

Access Control Lists define:
- Who can access specific resources.

Organizations should:
- Restrict access to authorized individuals only.

---

# Best Practices for Access Controls

Organizations should:

- Grant access only when necessary
- Regularly review permissions
- Remove unnecessary access
- Monitor privileged users

---

# SharePoint Online Example

For sensitive SharePoint sites:

- Only approved users should have access.
- Users should receive minimum required permissions.
- Permissions should be reviewed regularly.

---

# Least Privilege Principle

Least privilege means:
- Users receive only the minimum permissions required.

Examples:
- View access instead of Edit access
- Read-only permissions when possible

---

# Benefits of Least Privilege

Least privilege:
- Reduces attack surfaces
- Limits accidental exposure
- Minimizes damage from compromised accounts

---

# External Sharing Policies

Organizations can configure Microsoft 365 to:
- Restrict sharing with external users.

This helps prevent:
- Data leakage
- Unauthorized file sharing

---

# Balancing Security and Productivity

Restrictive sharing policies improve security, but organizations must:
- Balance protection with collaboration needs.

---

# Data Classification Schemes

Organizations should classify data based on sensitivity levels.

Common classifications include:

- High business impact
- Medium business impact
- Low business impact

---

# Why Data Classification Matters

Classification helps organizations:

- Identify sensitive information
- Apply protection policies
- Monitor high-risk data
- Enforce compliance requirements

---

# SharePoint and OneDrive Classification

Organizations can require users to:
- Tag documents and sites with classification labels.

Examples include:
- Confidential
- Internal
- Public
- Highly Sensitive

---

# Microsoft Purview Data Loss Prevention (DLP)

Microsoft Purview DLP helps organizations:
- Prevent sensitive information from leaving the tenant.

---

# DLP Capabilities

DLP can:

- Block sensitive emails
- Prevent unauthorized sharing
- Detect personal information
- Monitor risky behavior
- Enforce compliance policies

---

# Examples of Sensitive Data Protected by DLP

DLP policies can protect:

- Credit card numbers
- Social Security numbers
- Bank account details
- Financial records
- Healthcare information

---

# Email Protection with DLP

DLP can stop users from:
- Sending confidential documents externally.

It can also:
- Warn users before sharing sensitive information.

---

# Auditing and Monitoring

Organizations should enable:

- Auditing
- Alerts
- Activity monitoring

to detect suspicious activity quickly.

---

# Advanced Security Monitoring

Advanced Security Management helps organizations:

- Detect unusual behavior
- Identify risky activities
- Investigate threats
- Monitor cloud applications

---

# Suspicious Activity Indicators

Potential signs of data exfiltration include:

- Large file downloads
- Unusual sharing activity
- External forwarding
- Multiple failed sign-ins
- Unexpected administrator actions

---

# Security Best Practices

Organizations should:

- Enable MFA
- Implement DLP policies
- Use least privilege access
- Restrict external sharing
- Classify sensitive data
- Review access permissions regularly
- Monitor user activities

---

# Comprehensive Protection Strategy

Effective protection against data exfiltration combines:

- Identity security
- Access management
- Data classification
- DLP policies
- Monitoring and alerts
- User awareness training

---

# Key Takeaway

Data exfiltration occurs when attackers move sensitive information out of an organization's Microsoft 365 tenant. Organizations can reduce risk by securing accounts, enforcing least privilege, restricting sharing, classifying data, implementing Microsoft Purview DLP, and continuously monitoring for suspicious activity.
