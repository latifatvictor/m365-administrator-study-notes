## Microsoft Defender for Cloud Apps Summary

### Overview:
- A **cloud security solution (CASB)** that protects Microsoft and third-party cloud apps
- Provides:
  - Visibility
  - Data control
  - Threat protection
  - Compliance management
  - Automation and centralized control

---

### Core Capabilities:

#### 1. Shadow IT Discovery
- Identifies all cloud apps in use (25,000+ catalog)
- Assesses apps using **80+ risk factors**
- Allows:
  - Sanctioning (approved apps)
  - Unsanctioning (blocked apps)

---

#### 2. Data Protection
- Classifies and protects sensitive data in the cloud
- Applies policies to prevent:
  - Data exposure
  - Data leaks

---

#### 3. Threat Protection
- Detects anomalies and risky behavior such as:
  - Compromised accounts
  - Ransomware
  - Rogue apps
- Uses analytics and automation for remediation

---

#### 4. Compliance Management
- Ensures apps meet regulatory standards
- Prevents data use in non-compliant apps

---

## Architecture Components:

### 1. Cloud Discovery
- Analyzes traffic logs to identify cloud app usage
- Supports manual upload or continuous monitoring

---

### 2. App Connectors
- Connect via APIs to cloud apps
- Provides:
  - Activity monitoring
  - Threat detection
  - Policy enforcement
- Uses ML to generate alerts and insights

---

### 3. Conditional Access App Control
- Uses **reverse proxy** for real-time control
- Inspects traffic before reaching apps
- Enables:
  - Block unsafe downloads
  - Encrypt sensitive data
  - Monitor unmanaged devices
  - Restrict risky access (e.g., IP
