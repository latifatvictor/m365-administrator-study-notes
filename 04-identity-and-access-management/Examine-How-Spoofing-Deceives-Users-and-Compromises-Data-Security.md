# Examine How Spoofing Deceives Users and Compromises Data Security

## Overview

Spoofing is a cyberattack technique in which attackers falsify sender information to make emails appear as though they came from a trusted person, company, or domain. Spoofing is a cyberattack technique that falsifies sender information to make emails appear legitimate. Attackers commonly use spoofing in phishing and business email compromise attacks to steal credentials, spread malware, and compromise sensitive data. Microsoft 365 protects organizations against spoofing through Exchange Online Protection, Spoof Intelligence, and email authentication technologies such as SPF, DKIM, and DMARC.

Attackers use spoofing to:
- Trick users
- Deliver phishing emails
- Steal credentials
- Spread malware
- Compromise sensitive data

---

# What Is Spoofing?

Spoofing occurs when:
- An attacker forges sender information

to make an email:
- Appear legitimate
- Look trustworthy
- Mimic a known sender

---

# SMTP and Email Spoofing

Spoofing is possible because:
- SMTP (Simple Mail Transfer Protocol)

allows:
- One domain to send messages representing another domain

---

# Why Spoofing Exists

There are:
- Legitimate business uses
- Malicious attacker uses

for spoofing.

---

# Legitimate Internal Spoofing Scenarios

Organizations may legitimately spoof internal domains when:

- Third-party providers send employee surveys
- Marketing companies send company updates
- Assistants send emails on behalf of executives
- Internal applications send automated notifications

---

# Legitimate External Spoofing Scenarios

Organizations may legitimately spoof external domains when:

- Mailing lists relay messages
- SaaS providers send automated reports
- External systems send messages for partner organizations

---

# Malicious Spoofing

Attackers abuse spoofing to:

- Send phishing emails
- Deliver spam
- Trick users
- Steal credentials
- Spread malware

---

# Purpose of Spoofing Attacks

Spoofing attacks attempt to:

- Gain trust
- Create urgency
- Bypass suspicion
- Convince users to act quickly

---

# Common Spoofing Targets

Attackers commonly impersonate:

- Banks
- Microsoft
- IT departments
- Delivery companies
- Executives
- HR departments
- Trusted vendors

---

# Spoofing and Phishing

Spoofing is commonly used with:
- Phishing attacks

The spoofed sender helps attackers:
- Convince users the message is legitimate

---

# How Spoofing Works

Attackers modify:
- Email headers
- Sender addresses

so the message appears to come from:
- A trusted domain

---

# Email Sender Addresses

Email messages contain two important sender addresses:

- 5321.MailFrom
- 5322.From

---

# 5321.MailFrom

The:
- Sending mail server

uses:
- 5321.MailFrom

This address appears as:

```text
Return-Path
