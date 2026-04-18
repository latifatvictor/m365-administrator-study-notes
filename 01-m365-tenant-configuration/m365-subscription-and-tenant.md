# Microsoft 365 Subscription, Plans & Microsoft Entra Tenant

---

## 🔑 Key Concepts (Must Know)

### Plan vs Subscription

- **Plan** = Features and services (e.g. E3, E5)
- **Subscription** = Paid access to a plan

👉 Interview Tip:  
A plan defines *what you get*, a subscription defines *how you access it*

---

### Microsoft 365 Subscription

- Provides access to cloud services:
  - Exchange Online (email)
  - SharePoint Online (file storage)
  - OneDrive for Business
  - Microsoft Teams
- Includes licenses assigned to users
- Managed via Microsoft 365 Admin Center

👉 Real-world:
You assign licenses so users can access email, Teams, etc.

---

### Microsoft Entra Tenant (CRITICAL)

- Identity and access management foundation
- Automatically created when a subscription is purchased
- Stores:
  - Users
  - Groups
  - Domains
  - Security policies

👉 Key idea:
**Tenant = container**
**Subscription = services you pay for**

---

## 🔗 Relationship Between Subscription & Tenant

- 1 Microsoft 365 subscription → 1 Microsoft Entra tenant
- Tenant handles:
  - Authentication (sign-in)
  - Authorization (access control)

👉 Real-world:
User signs into Outlook or Teams → validated by Entra ID

---

## 📦 Licensing (Very Common in IT Support)

### Key Points

- Licenses are per user (mostly)
- Assigned via Admin Center
- Can be:
  - Added
  - Removed
  - Reassigned

### Typical Workflow

- New starter → assign license  
- Leaver → remove license  
- Role change → update license  

👉 Interview Tip:
License management = cost + access control

---

## 🧠 Types of Microsoft 365 Plans

### Enterprise Plans
- **E3** → Standard enterprise features  
- **E5** → Advanced security + compliance  

### Business Plans
- **Business Basic** → Web apps only  
- **Business Standard** → Desktop apps included  

### Frontline Plans
- **F1 / F3** → Limited access users  

👉 Important:
E5 = security-heavy (Defender, Compliance, Identity Protection)

---

## ⚠️ Plans That Don’t Fully Create a Tenant

Some plans:
- Provide limited Entra functionality
- Are often combined with others

Examples:
- EMS E5  
- Microsoft 365 Apps  
- Business Basic / Standard  

👉 Real-world:
You often combine EMS + E3/E5 for full capability

---

## 🏢 Multiple Tenants (Enterprise Reality)

Organizations may have multiple tenants due to:

- Mergers & acquisitions  
- Different departments  
- Compliance requirements  
- Legacy environments  

👉 Challenge:
More complexity in:
- User management  
- Licensing  
- Administration  

---

## 🌐 Tenant Details

- Default domain:
  - company.onmicrosoft.com  
- Can add up to **900 domains**
- Tenant tied to:
  - region (data location)

👉 Real-world:
Used for email domains (e.g. user@company.com)

---

## 🏗️ What Makes a Well-Designed Tenant

### Core Areas

#### Licensing
- Correct plan selection (E3 vs E5)
- Enough licenses for users

#### Identity & Security
- MFA enabled
- Conditional Access policies
- Secure authentication

#### Networking
- Correct DNS configuration
- Optimised traffic (VPN / remote users)

#### Hybrid Identity (if applicable)
- Azure AD Connect sync
- AD DS integration

#### Device Management
- Intune configured
- Device compliance policies

#### Application & Data
- Exchange Online configured
- SharePoint / OneDrive setup
- Teams deployment

---

## 🔥 Interview Questions

### Q1: What is the difference between a tenant and a subscription?

👉 Answer:
A subscription is the paid service that provides access to Microsoft 365 features, while a tenant is the identity and management container that holds users, data, and configurations.

---

### Q2: What happens when a company buys Microsoft 365?

👉 Answer:
A Microsoft Entra tenant is created automatically, allowing administrators to manage users, assign licenses, and configure services.

---

### Q3: Why would a company have multiple tenants?

👉 Answer:
Due to mergers, compliance needs, different business units, or legacy environments.

---

### Q4: What is your role in license management?

👉 Answer:
Assign licenses to new users, remove them for leavers, and ensure users have the correct access based on their role.

---

## 💼 Real-Life IT Tasks

- Creating users in Admin Center  
- Assigning licenses  
- Troubleshooting login issues  
- Managing domains  
- Supporting MFA setup  
- Checking tenant settings  

---

## 🧠 Summary

- Plan = features  
- Subscription = access  
- Tenant = identity foundation  

👉 Everything in Microsoft 365 depends on the **tenant**
