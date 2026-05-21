## Onboard Devices in Microsoft Defender for Endpoint Summary

### Overview:
- Onboarding connects devices to **Microsoft Defender for Endpoint (MDE)**
- Enables:
  - Threat detection
  - Risk assessment
  - Reporting to Intune
- Works with:
  - ✅ Windows 10/11  
  - ✅ Android  
  - ✅ iOS/iPadOS  

---

## Onboarding Methods:

### Windows Devices:
- Use:
  - **Endpoint Detection & Response (EDR) policy** (recommended)
  - Device configuration profile
  - Group Policy / Configuration Manager

- Key setting:
  - **Auto from connector** (automatic onboarding package)

---

### macOS:
- Onboard via **Defender for Endpoint integration**
- Enables risk monitoring and reporting

---

### Android / iOS:
- No onboarding package
- Use:
  - Defender app installation
  - Intune app protection policies
- iOS (Supervised Mode):
  - Configure via **App configuration policy**

---

## Compliance Policy (Risk Levels):
- Intune defines acceptable risk levels
- MDE evaluates actual risk

### Risk Levels:
- **Clear (Secure)** → No threats (most secure)  
- **Low** → Only low threats allowed  
- **Medium** → Low + medium threats allowed  
- **High** → All threats allowed (least secure)  

- Noncompliant devices → restricted access

---

## App Protection Policies (Mobile):
- Protect app data on unmanaged/enrolled devices
- Enforce:
  - Max allowed device threat level
  - Actions:
    - Block access
    - Wipe corporate data

---

## Conditional Access:
- Uses device compliance data from Intune + MDE
- Blocks access if device risk exceeds threshold
- Applies to:
  - SharePoint
  - Exchange Online
  - Other cloud apps

---

## Security Flow:
1. Device onboarded → sends telemetry  
2. MDE analyzes activity → assigns risk level  
3. Intune compares risk vs compliance policy  
4. If noncompliant → Conditional Access blocks access  

---

## Key Roles:
- **MDE:** Risk analysis & threat detection  
- **Intune:** Policy enforcement & device management  
- **Entra ID:** Conditional Access enforcement  

---

## Key Takeaway:
Onboarding devices enables **end-to-end security** where Microsoft Defender for Endpoint detects threats, Intune enforces compliance, and Conditional Access blocks risky devices from accessing corporate resources.
