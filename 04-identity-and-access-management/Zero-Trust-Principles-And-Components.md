# Examine the Principles and Components of the Zero Trust Model

## Overview

Zero Trust is a modern security strategy designed to protect organizations in today’s cloud-first and hybrid work environments.

Traditional security models assumed:
- Everything inside the corporate network could be trusted.

Zero Trust changes this approach by assuming:
- Every request may be malicious.
- Every access attempt must be verified.

Core philosophy:
Never trust, always verify

---

# What is Zero Trust?

Zero Trust is a security model that:
- Assumes breach by default
- Requires continuous verification
- Protects identities, devices, applications, networks, and data

Every request must be:
- Authenticated
- Authorised
- Encrypted

before access is granted.

---

# Core Principles of Zero Trust

The Zero Trust model is built on three foundational principles:

1. Verify explicitly
2. Use least privileged access
3. Assume breach

---

# Principle 1: Verify Explicitly

Organizations should always authenticate and authorise access requests.

Verification should use all available signals, including:

- User identity
- Device health
- Location
- Application
- Service or workload
- Data sensitivity
- User behaviour
- Risk signals
- Anomalies

---

# Principle 2: Use Least Privileged Access

Users should receive only the minimum permissions required.

This reduces:
- Attack surface
- Insider risk
- Lateral movement

Least privilege can include:
- Just-In-Time access
- Just-Enough-Access
- Role-Based Access Control
- Conditional Access
- Adaptive risk-based policies

---

# Principle 3: Assume Breach

Zero Trust assumes attackers may already exist inside the network.

Organizations should:
- Minimise damage
- Prevent lateral movement
- Detect anomalies quickly
- Encrypt sessions end to end
- Use analytics for threat detection

---

# Zero Trust Components

Microsoft identifies six foundational Zero Trust components:

1. Identities
2. Endpoints
3. Applications
4. Data
5. Infrastructure
6. Networks

---

# 1. Secure Identities

Identities form the Zero Trust control plane.

Identities may represent:
- Users
- Services
- Applications
- IoT devices

Organizations should:
- Use strong authentication
- Enable MFA
- Enforce Conditional Access
- Apply least privilege
- Monitor identity risks

---

# 2. Secure Endpoints

Endpoints include:
- PCs
- Mobile devices
- Servers
- IoT devices
- BYOD devices

Organizations should:
- Monitor device compliance
- Assess device health
- Enforce security baselines
- Restrict risky devices

---

# 3. Secure Applications

Applications and APIs provide access to organizational data.

Applications may include:
- SaaS apps
- Cloud apps
- On-premises apps
- APIs

Organizations should:
- Discover shadow IT
- Control app permissions
- Monitor abnormal behaviour
- Secure configurations
- Restrict risky activities

---

# 4. Secure Data

Data is the main asset organizations protect.

Data should remain protected even outside corporate environments.

Organizations should:
- Classify data
- Label data
- Encrypt data
- Apply DLP policies
- Restrict access

---

# 5. Secure Infrastructure

Infrastructure includes:
- Servers
- Virtual machines
- Containers
- Cloud services
- Microservices

Organizations should:
- Harden systems
- Apply patches
- Monitor telemetry
- Detect anomalies
- Use Just-In-Time administration

---

# 6. Secure Networks

Networks connect users, devices, applications, and services.

Zero Trust networking focuses on:
- Visibility
- Segmentation
- Encryption
- Monitoring
- Analytics

Organizations should:
- Segment networks
- Use microsegmentation
- Apply real-time threat protection
- Monitor traffic
- Prevent lateral movement

---

# Trust-by-Default vs Trust-by-Exception

Traditional security:
- Trust by default

Zero Trust:
- Trust by exception

This means no user, device, application, or network connection is automatically trusted.

---

# Benefits of Zero Trust

Zero Trust helps organizations achieve:

- Better visibility
- Reduced attack surface
- Improved threat detection
- Reduced insider risk
- Better compliance
- Stronger cloud security
- Improved remote work security

---

# Microsoft Zero Trust Guidance

Microsoft recommends organizations:

- Assess current security posture
- Secure identities first
- Secure endpoints
- Protect applications
- Protect data
- Harden infrastructure
- Segment networks
- Monitor continuously

---

# Key Takeaway

Zero Trust is based on the principle of “never trust, always verify.” It requires organizations to continuously authenticate, authorise, monitor, and secure identities, devices, applications, data, infrastructure, and networks. The model assumes breach, applies least privilege, and uses analytics and continuous verification to protect modern hybrid environments.

