## Microsoft Purview Information Barriers (IB) – Summary

### Overview:
- Microsoft 365 enables collaboration but also provides controls to **restrict communication when necessary**
- **Information Barriers (IB)** is a Microsoft Purview feature that:
  - Restricts **two-way communication and collaboration**
  - Helps prevent:
    - Conflicts of interest  
    - Insider trading  
    - Data leakage between internal groups  

---

## What Are Information Barriers?
- A **compliance solution** that controls:
  - Who can communicate  
  - Who can share data  
- Ensures:
  - Only authorized users interact with sensitive data  
  - Access is based on business need or regulation  

---

## Supported Services:
- ✅ Microsoft Teams  
- ✅ SharePoint Online  
- ✅ OneDrive for Business  

---

## Key Concept: Segments
- A **segment** = logical group of users
- Based on:
  - Department  
  - Job role  
  - Business unit  

---

### Example:
- **Finance segment**
  - Access to financial data  
  - Restricted from Marketing  
- **Marketing segment**
  - Does not access Finance data  

✅ Policies applied per segment  

---

## Use Cases:
- Restrict communication between departments  
- Prevent insider trading risks  
- Limit file sharing across teams  
- Control collaboration with sensitive data  

---

## Key Capabilities:
- Block:
  - Chat and calls  
  - File sharing  
  - Team membership  
- Restrict:
  - Access to sites and content  
  - User discovery/search  

---

## Important Limitation:
- ❗ Only supports **two-way restrictions**
  - Team A ↔ Team B → both blocked  
- ❌ Does NOT support one-way restrictions  

---

## How IB Policies Work:
- Policies enforce restrictions in real-time
- Microsoft Purview checks:
  - Communication attempts  
  - File sharing actions  
- Allows or blocks based on policy rules  

---

## Microsoft Teams Restrictions:
