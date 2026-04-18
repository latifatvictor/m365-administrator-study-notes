# Configure Tenant-Level Sharing (SharePoint & OneDrive)

---

## 🔑 Key Concepts (Must Know)

### What is External Sharing?

External sharing allows users to:

- Share files, folders, and sites  
- With people outside the organisation (guests)  

👉 Examples:
- Clients  
- Vendors  
- Partners  

---

## ⚠️ Default Behaviour

- External sharing is **ON by default**

👉 Best practice:
Turn it OFF initially until policies are defined

---

## 🧠 Why It Matters

- Enables collaboration  
- Introduces security risks  
- Requires proper governance  

👉 Real-world:
Too open = data leak  
Too restricted = poor collaboration  

---

## ⚙️ Where to Configure

👉 SharePoint Admin Center

Path:
Admin Center → SharePoint → Policies → Sharing

---

## 🔗 Key Rule (VERY IMPORTANT)

👉 Organization-level setting controls everything  

- Site-level sharing cannot be MORE permissive  
- Only same or MORE restrictive  

👉 Example:
Org = "Existing guests only"  
Site = cannot be "Anyone"

---

## 🔐 Sharing Levels (CRITICAL)

### 1. Anyone (Least Secure)

- No login required  
- Link-based access  

👉 Risk:
Cannot track who accessed files  

👉 Use case:
Non-sensitive public sharing  

---

### 2. New and Existing Guests

- Users must sign in  
- Guests added to directory  

👉 Best balance:
Security + collaboration  

---

### 3. Existing Guests

- Only pre-approved guests  

👉 More controlled environment  

---

### 4. Only People in Your Organization (Most Secure)

- External sharing OFF  

👉 Use case:
Sensitive data  

---

## 🧠 Important Rule

👉 OneDrive can be MORE restrictive than SharePoint  
👉 But NOT more permissive  

---

## 🔐 Microsoft Entra Integration

External sharing depends on:

- Entra ID guest settings  
- Azure B2B collaboration  

👉 Always review BOTH:
- SharePoint settings  
- Entra settings  

---

## ⚙️ Advanced Sharing Controls

### Domain Restrictions

- Allow or block specific domains  

👉 Example:
Allow: partner.com  
Block: gmail.com  

---

### Group-Based Sharing

- Only specific users can share externally  

👉 Improves governance  

---

### Guest Restrictions

- Guests must use invited email  
- Prevents account switching  

---

### Guest Expiry

- Automatically remove access after X days  

👉 Real-world:
Temporary vendor access  

---

## 🔗 File & Folder Link Settings

### Link Types

#### Specific People (Most Secure)
- Named users only  

---

#### People in Organisation
- Internal sharing  

---

#### Anyone with Link (Least Secure)
- No authentication  

---

👉 Important:
Default link type affects user behaviour  

---

## ⏳ Anyone Link Controls

- Set expiration (e.g. 7 days)  
- Restrict permissions (view only)  

👉 Best practice:
Always enforce expiry  

---

## 📊 Other Settings

### View Tracking

- Show who viewed files  

👉 Useful for:
- Auditing  
- Monitoring usage  

---

### Short Links

- Generates shorter URLs  

👉 Useful for integrations  

---

## 💼 Real-Life IT Tasks

- Restrict external sharing globally  
- Allow sharing only to trusted domains  
- Troubleshoot “user can’t share file externally”  
- Set expiration for guest access  
- Configure secure sharing policies  

---

## ⚠️ Common Mistakes

- Leaving "Anyone" sharing enabled globally  
- Not configuring expiration policies  
- Ignoring Entra guest settings  
- Allowing all users to share externally  

---

## 🔥 Interview Questions

### Q1: What happens if site and org sharing settings conflict?

👉 Answer:
The most restrictive setting is applied.

---

### Q2: What is the safest sharing option?

👉 Answer:
Only people in your organization.

---

### Q3: How do you securely allow external collaboration?

👉 Answer:
Use "New and existing guests" with authentication and apply expiration policies.

---

### Q4: Why is "Anyone link" risky?

👉 Answer:
It allows anonymous access and cannot track who accessed the data.

---

## 🧠 Summary

- External sharing must be controlled carefully  
- Organization-level settings override everything  
- Always balance:
  - Security  
  - Collaboration  

👉 Sharing misconfiguration = major security risk
