# Microsoft 365 Network Connectivity Assessments and Insights

---

## 📌 What It Is

Microsoft 365 Network Connectivity provides tenant-level network performance insights in the Microsoft 365 admin centre.

Location:
Health → Network connectivity

It helps admins understand how network design affects Microsoft 365 user experience.

---

## 🎯 Main Purpose

- Assess network performance
- Identify connectivity issues
- Improve Microsoft 365 user experience
- Provide location-based recommendations
- Help optimise office network design

---

## 📊 Network Assessment Score

- Score range: 0–100
- Available for:
  - Entire tenant
  - Individual office locations

Higher score = better Microsoft 365 network performance

---

## 📍 Location Data Requirements

To see useful assessments, Microsoft must identify office locations.

Options:

1. Windows Location Services  
2. Manual location upload  
3. Microsoft 365 network connectivity test  

---

## 🧭 Option 1: Windows Location Services

- Automatically detects office locations
- Requires supported Windows devices
- Needs up-to-date OneDrive client
- Requires Wi-Fi for accurate location
- Location Services must be enabled

Important:
- Locations are detected at city level
- Data may appear after 24 hours

---

## 🧭 Option 2: Manually Add Locations

Admins can manually add office locations using:

- LAN subnet
- Public egress IP
- CSV upload

Best when:
- Multiple offices exist in one city
- You need accurate site names
- You know subnet details

---

## 🧭 Option 3: Run Network Connectivity Test

A user at each office runs the Microsoft 365 network connectivity test.

Useful for:
- Quick testing
- Location-specific troubleshooting
- Confirming performance issues

Results can appear within minutes.

---

## 👤 Required Admin Roles

Read access:
- Reports Reader

Configure locations/settings:
- Service Support Administrator

---

## ⚠️ Important Limitation

Currently supported in:
- Worldwide commercial tenants

Not supported in:
- GCC Moderate
- GCC High
- DoD
- China

---

## 🔍 Common Network Insights

### 1. Backhauled Network Egress

Traffic exits far away from user location.

Issue:
- Higher latency
- Poor Microsoft 365 performance

Fix:
- Use local internet breakout

---

### 2. Network Intermediary Device

Detected devices such as:

- Proxy
- VPN
- DLP appliance

Issue:
- Adds latency
- Can affect reliability

Fix:
- Bypass Microsoft 365 traffic where appropriate

---

### 3. Better Performance Detected Nearby

Other tenants in same region perform better.

Possible causes:
- ISP issues
- Network bottlenecks
- Poor routing

---

### 4. Non-Optimal Exchange Online Front Door

Users connect to a less suitable Exchange Online entry point.

Fix:
- Improve DNS and egress alignment
- Use local/direct internet egress

---

### 5. Non-Optimal SharePoint Online Front Door

Users connect to a less suitable SharePoint service front door.

Fix:
- Align DNS resolver with egress location
- Avoid backhauling

---

### 6. Low SharePoint Download Speed

Download speed below 1 MBps.

Possible causes:
- Bandwidth limits
- Congestion
- Poor routing

---

## 💼 Real Work Scenarios

### Scenario 1: Teams Calls Poor in One Office
Check Network Connectivity insights for:
- Backhauling
- Proxy/VPN
- Local egress issues

---

### Scenario 2: SharePoint Slow for London Users
Review:
- SharePoint front door
- Download speed
- Local latency

---

### Scenario 3: Outlook Slow in Regional Office
Check:
- Exchange front door
- DNS resolver location
- Network egress point

---

## 🔐 Best Practices

- Keep network egress close to users
- Avoid unnecessary proxy inspection for Microsoft 365 traffic
- Align DNS resolver with network egress
- Use direct local internet breakout
- Monitor location-based insights regularly
- Review recommendations in admin centre
- Use network tests during troubleshooting

---

## ⚠️ Common Mistakes

- Backhauling Microsoft 365 traffic through head office
- Using remote DNS resolvers
- Routing traffic through unnecessary proxies
- Ignoring location-specific network issues
- Not configuring office locations
- Assuming all Microsoft 365 issues are service outages

---

## 🎯 Interview Questions

Q1: Where do you view Microsoft 365 network connectivity insights?  
Microsoft 365 admin centre → Health → Network connectivity

---

Q2: What does the network assessment score show?  
How network connectivity affects Microsoft 365 user experience.

---

Q3: What is backhauled network egress?  
When user traffic exits the network far away from the user location.

---

Q4: Why is local internet breakout important?  
It reduces latency and improves Microsoft 365 performance.

---

Q5: What can cause non-optimal service front door usage?  
Network backhauling or misaligned DNS resolver configuration.

---

Q6: What role can configure network connectivity settings?  
Service Support Administrator.

---

## 🧠 Summary

- Network connectivity affects Microsoft 365 performance
- Microsoft provides location-based assessments and insights
- The goal is to reduce latency and improve user experience
- Local egress and correct DNS design are critical
- Network insights help identify real-world performance issues

---
