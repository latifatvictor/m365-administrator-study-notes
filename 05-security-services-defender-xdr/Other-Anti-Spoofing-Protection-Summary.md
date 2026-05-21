# Explore Other Anti-Spoofing Protection - Summary

## Overview

Exchange Online Protection (EOP) includes built-in:
- Anti-spoofing protection
- Anti-phishing protection

However, because some spoofing scenarios are legitimate and others are malicious, EOP also relies on additional email authentication technologies to verify senders and prevent phishing attacks.

Microsoft recommends implementing all three email authentication methods:
1. SPF
2. DKIM
3. DMARC

Together, these technologies provide stronger protection against spoofing and phishing attacks.

---

# Why Spoofing Exists

SMTP supports spoofing by design for legitimate business purposes such as:
- Third-party marketing services sending mail on behalf of a company
- Internal applications sending automated notifications
- Delegated email sending

Unfortunately, attackers also abuse spoofing to:
- Steal credentials
- Deliver phishing emails
- Trick users into sharing sensitive information

---

# Sender Policy Framework (SPF)

## What is SPF?

SPF is:
- A DNS TXT record

Purpose:
- Validates authorized sending mail servers

SPF verifies:
- The sender’s IP address
- Against the domain owner’s approved mail servers

---

# How SPF Works

1. Sender sends email
2. Receiving server checks SPF TXT record in DNS
3. Server validates sending IP address
4. Message either:
   - Passes SPF
   - Fails SPF

---

# SPF Benefits

SPF helps:
- Prevent spoofing
- Reduce phishing
- Validate legitimate senders

---

# Important SPF Notes

Organizations may need to update SPF records when:
- Using hybrid Exchange environments
- Configuring DKIM or DMARC
- Hitting DNS lookup limits
- Using third-party senders

---

# SPF Limitations

SPF only validates:
```text
5321.MailFrom

This means:

Attackers can still spoof displayed sender addresses

Because of this limitation:

DKIM and DMARC are also required
DomainKeys Identified Mail (DKIM)
What is DKIM?

DKIM:

Adds digital signatures to email messages

Purpose:

Verifies email integrity
Confirms email authenticity
Prevents message tampering
How DKIM Works
Sending server signs message using private key
Public key published in DNS
Receiving server validates signature

If signature matches:

Message is trusted
DKIM Benefits

DKIM helps:

Prevent domain spoofing
Detect tampered emails
Improve sender trust
When to Configure DKIM Manually

Microsoft recommends manual DKIM configuration when:

Using multiple custom domains
Planning to use DMARC
Using third-party email services
Wanting custom DKIM control
Microsoft 365 DKIM Defaults

Microsoft 365 automatically:

Creates DKIM keys
Signs email for onmicrosoft.com domains

Custom domains:

Can also use Microsoft-managed DKIM
Domain-based Message Authentication, Reporting, and Conformance (DMARC)
What is DMARC?

DMARC:

Builds on SPF and DKIM

Purpose:

Verifies displayed sender address
Defines handling for failed authentication

DMARC protects:

5322.From

which is:

The visible sender users see in Outlook
DMARC Benefits

DMARC helps:

Prevent phishing
Prevent impersonation
Improve trust
Enforce authentication policies
DMARC TXT Record

DMARC uses:

DNS TXT records

Example:

v=DMARC1; p=none;
DMARC Policy Actions
Policy	Meaning
none	Monitor only
quarantine	Send suspicious mail to junk/quarantine
reject	Reject suspicious mail
How SPF and DMARC Work Together
SPF Checks

SPF validates:

5321.MailFrom
DMARC Checks

DMARC validates:

5322.From
Example Attack Scenario

Attacker sends:

MailFrom: phish@phishing.contoso.com
From: security@woodgrovebank.com

SPF may pass:

Because phishing.contoso.com is valid

But DMARC fails:

Because woodgrovebank.com authentication fails

Result:

Message identified as suspicious
Key Email Addresses
Address	Purpose
5321.MailFrom	Handles bounce messages
5322.From	Visible sender users see
Why DMARC is Important

Without DMARC:

Users may see spoofed sender addresses
SPF alone cannot fully stop phishing
EOP Email Authentication Stack

Microsoft 365 anti-spoofing uses:

SPF
DKIM
DMARC
EOP spoof intelligence
Anti-phishing policies
Best Practices

Microsoft recommends:

Configure SPF
Configure DKIM
Configure DMARC
Use all three together
Review authentication reports regularly
Configure proper DNS records
Monitor phishing activity
Security Benefits

These protections help organizations:

Prevent spoofing attacks
Reduce phishing
Protect credentials
Improve email trust
Protect brand reputation
Improve email deliverability
Key Exam Points
Technology	Purpose
SPF	Validates sending IP addresses
DKIM	Verifies email integrity
DMARC	Validates visible sender address
5321.MailFrom	Bounce address
5322.From	Visible sender address
Important Concepts
SPF

Checks:

Sending mail server legitimacy
DKIM

Checks:

Message was not altered
DMARC

Checks:

Sender alignment and authentication
Final Summary

Exchange Online Protection (EOP) uses:

SPF
DKIM
DMARC

to strengthen anti-spoofing and anti-phishing protection.

Together, these technologies:

Validate senders
Verify message integrity
Protect displayed sender addresses
Reduce phishing attacks
Improve Microsoft 365 email security

Microsoft recommends implementing:

SPF
DKIM
DMARC

together for maximum protection.

Knowledge Check Answer

Q: Which third email authentication technique works with DKIM and DMARC to help prevent spoofing and phishing?

Answer:

Sender Policy Framework (SP
