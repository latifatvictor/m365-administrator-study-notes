# SharePoint Guest Collaboration (Microsoft 365)

---

## 🔑 Overview

SharePoint allows organisations to collaborate with external users (guests) on:

- documents  
- lists  
- data  
- team sites  

👉 Modern SharePoint sites are connected to Microsoft 365 Groups, which control access and permissions.

---

## 🧠 Key Concept

Guest collaboration in SharePoint depends on multiple layers:

1. Microsoft Entra ID (B2B settings)  
2. Microsoft 365 Groups settings  
3. SharePoint organisation settings  
4. SharePoint site-level settings  

👉 If one layer blocks access → guest collaboration fails

---

# ⚙️ Step 1: Configure Microsoft Entra External Collaboration

Location:

Microsoft Entra Admin Center → External Identities → External collaboration settings  

---

### ✅ Required Settings

Enable one of:

- Members can invite guests  
- Anyone in organisation can invite guests  

---

### 🔐 Security Controls

- Restrict guest directory visibility  
- Allow/block specific domains  

---

👉 Important:
If guest access is blocked here → nothing else works

---

# ⚙️ Step 2: Configure Microsoft 365 Groups Guest Access

Location:

Microsoft 365 Admin Center → Settings → Org settings → Microsoft 365 Groups  

---

### ✅ Enable BOTH:

- Allow group owners to add external users  
- Allow guests to access group content  

---

👉 Without this:
Guests cannot access SharePoint team sites

---

# ⚙️ Step 3: Configure SharePoint Organisation-Level Sharing

Location:

SharePoint Admin Center → Policies → Sharing  

---

### 🔓 Sharing Options

| Option | Description |
|------|------------|
| Anyone | Anonymous access (no sign-in required) |
| New and existing guests | Authenticated external users |
| Existing guests | Only previously invited users |
| Only people in your organisation | No external sharing |

---

👉 Best Practice:
Use **New and existing guests** for security

---

# ⚙️ Step 4: Create SharePoint Site

Steps:

1. SharePoint Admin Center  
2. Sites → Active sites  
3. Click Create  
4. Select Team site  
5. Add site name and owner  
6. Choose Public or Private  
7. Finish  

---

👉 This creates:

- SharePoint site  
- Microsoft 365 Group  
- Shared resources  

---

# ⚙️ Step 5: Configure Site-Level Sharing

Location:

SharePoint Admin Center → Sites → Active sites → Select site  

---

### Important Rule

Site settings CANNOT be more permissive than organisation settings  

---

### Recommended Setting

- New and existing guests  

---

👉 Use this to:

- enforce authentication  
- control access at site level  

---

# ⚙️ Step 6: Invite Guest Users

Steps:

1. Go to SharePoint site  
2. Click Members  
3. Click Add members  
4. Enter email address  
5. Send invite  

---

👉 Result:

- Guest added to Microsoft 365 Group  
- Access granted to site  

---

## ⚠️ Important Notes

- Guests cannot be added directly from site in some cases → use group  
- Guests must accept invitation  
- Sharing settings affect files and folders differently  
- Sensitivity labels can restrict sharing further  

---

## 🔐 Security Best Practices

- Avoid "Anyone" sharing unless necessary  
- Restrict domains for external users  
- Use Conditional Access  
- Regularly review guest access  
- Apply sensitivity labels  

---

## 💼 Real-Life IT Scenarios

- sharing documents with vendors  
- collaborating with external partners  
- giving contractors access to project sites  
- troubleshooting “guest cannot access site”  
- restricting external sharing for sensitive teams  

---

## ⚠️ Common Issues

- guest cannot access site → Entra settings blocking  
- guest not receiving invite → email issue  
- guest sees nothing → permissions not assigned  
- sharing disabled at org level  
- group settings not enabled  

---

## 🔥 Interview Questions

### Q1: What controls SharePoint guest access?

Microsoft Entra ID, Microsoft 365 Groups, and SharePoint sharing settings.

---

### Q2: Why might guest access fail?

Because one of the layers (Entra, Groups, or SharePoint) is blocking access.

---

### Q3: What is the safest sharing option?

New and existing guests (requires authentication).

---

### Q4: Can site settings override organisation settings?

No, site settings cannot be more permissive.

---

### Q5: Where do you add guest users?

To the Microsoft 365 Group linked to the SharePoint site.

---

## 🧠 Summary

- SharePoint guest access is controlled by multiple layers  
- All layers must be correctly configured  
- Guests are added via Microsoft 365 Groups  
- Security should always be prioritised  

👉 SharePoint collaboration = powerful but must be controlled
