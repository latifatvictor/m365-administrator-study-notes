# Implement Anti-Spam Policies in Microsoft 365

## Overview

Exchange Online Protection (EOP) automatically protects email messages against:
- Spam
- Junk email
- Phishing
- Bulk mail

EOP uses:
- Proprietary spam filtering technologies
- Machine learning
- Heuristics
- Threat intelligence
- User feedback

to continuously improve spam detection.

---

# What is Spam Filtering?

Spam filtering:
- Identifies suspicious email
- Assigns a spam score
- Determines appropriate action

EOP processes:
- Inbound mail
- Outbound mail
- Internal mail (Exchange Online)

---

# Spam Confidence Level (SCL)

EOP assigns:
- Spam Confidence Level (SCL)

to each message.

The SCL value is:
- Added as an X-header

Higher SCL:
- Greater likelihood message is spam

---

# SCL Values and Default Actions

| SCL Value | Meaning | Default Action |
|---|---|---|
| -1 | Skipped spam filtering | Deliver to Inbox |
| 0,1 | Not spam | Deliver to Inbox |
| 5,6 | Spam | Move to Junk Email |
| 7,8,9 | High confidence spam | Junk or Quarantine |

---

# Why SCL Values 2, 3, and 4 Are Missing

Microsoft intentionally avoids:
- SCL 2
- SCL 3
- SCL 4

---

# SCL 2

Historically used for:
- Mail flow rule spam marking

Microsoft removed usage due to:
- Inconsistency
- Confusion

---

# SCL 3 and 4

Historically reserved for:
- DMARC failures
- Human analysis scenarios

Not widely used.

---

# Important Note About SCL 7

Spam filtering itself:
- Typically does NOT assign SCL 7

Other systems may assign it:
- Human analysts
- DMARC failures
- Mail flow rules

---

# Bulk Complaint Level (BCL)

BCL identifies:
- Bulk email
- Gray mail

Higher BCL:
- Greater likelihood of spam-like behavior

---

# Spam Filtering Verdicts

## Spam

Assigned:
- SCL 5 or 6

---

# High Confidence Spam

Assigned:
- SCL 7, 8, or 9

---

# Phishing

Phishing emails may:
- Be quarantined

Users:
- Cannot directly release phishing messages

---

# High Confidence Phishing

Always:
- Quarantined

Users:
- Cannot release messages themselves

---

# Bulk

Message exceeded:
- Configured BCL threshold

---

# Anti-Spam Message Headers

Headers help determine:
- Why message was flagged
- Why filtering was bypassed

---

# Reporting False Positives and False Negatives

Organizations can report:
- Good mail marked as spam
- Malicious mail delivered successfully

This improves:
- Microsoft detection systems

---

# Anti-Spam Policies

Anti-spam policies configure:
- Spam filtering settings
- Actions
- Thresholds
- Quarantine behavior

---

# Important Limitation

Organizations:
- Cannot completely disable spam filtering

---

# Bypassing Spam Filtering

Mail flow rules can:
- Bypass most spam filtering

Used when:
- Third-party mail filtering exists

---

# Important Security Note

Even if spam filtering is bypassed:
- Malware scanning still occurs
- High confidence phishing still filtered

---

# Hybrid Environment Requirement

Hybrid environments require:
- Transport rules

to recognize:
- EOP spam headers

---

# Recipient Filters in Anti-Spam Policies

Policies can apply to:

## Users

## Groups

## Domains

---

# Group Support

Supported:
- Distribution groups
- Mail-enabled security groups
- Microsoft 365 Groups

Not supported:
- Dynamic distribution groups

---

# Filter Logic

## Same Condition Type

Uses:
- OR logic

Example:
```text
recipient1 OR recipient2
