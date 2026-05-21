## Configure Microsoft Defender for Endpoint in Intune Summary

### Overview:
- Integrates **Microsoft Defender for Endpoint (MDE)** with **Microsoft Intune**
- Provides **Mobile Threat Defense (MTD)**
- Helps detect risks and enforce **conditional access based on device security**

---

## Supported Platforms:
- ✅ Windows 10/11  
- ✅ Android  
- ✅ iOS/iPadOS  

---

## Core Integration Steps:

### 1. Enable Service-to-Service Connection
- Connect Intune ↔ Defender for Endpoint
- Allows sharing of **device risk data**

---

### 2. Onboard Devices
- Use **device configuration profiles**
- Enables devices to send telemetry to MDE

---

### 3. Configure Device Compliance Policies
- Define acceptable **risk levels**
- Devices exceeding risk = **noncompliant**

---

### 4. Apply Conditional Access
- Block noncompliant/high-risk devices from:
  - Corporate apps
  - Organizational resources

---

### 5. Configure App Protection Policies
- For mobile devices (Android/iOS)
- Protect both:
  - Enrolled devices
  - Unenrolled devices

---

## Key Features Enabled:
- Threat & Vulnerability Management (TVM)
- Automated remediation using Intune
- Risk-based access control
- Endpoint security configuration (even for non-enrolled devices)

---

## Example Security Flow:
1. User opens malicious file  
2. MDE detects:
   - Suspicious activity
   - Privilege escalation
   - Remote access attempt  
3. Device marked **High Risk**
4. Intune compliance policy flags device as **Noncompliant**
5. Conditional Access blocks device access to corporate resources  

---

## Prerequisites:
- Microsoft Defender for Endpoint license  
- Microsoft Intune license  
- Admin role with Mobile Threat Defense permissions  

---

## Enable Integration (High-Level Steps):
1. Go to **Intune admin center → Endpoint security**
2. Select **Microsoft Defender for Endpoint**
3. Open Defender portal → **Advanced features**
4. Enable **Microsoft Intune connection**
5. Turn on platform connections:
   - Windows
   - Android
   - iOS/iPadOS
6. Save configuration

---

## Important Notes:
- Sync occurs approx. every **24 hours**
- Intune auto-creates **classic conditional access policies** (do not modify/delete)
- Extra iOS settings available for app visibility and vulnerability assessment

---

## Key Takeaway:
Integrating Defender for Endpoint with Intune enables **risk-based device compliance and access control**, ensuring only **secure devices can access organizational resources**.
