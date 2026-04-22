# Microsoft 365 Identity Models (Cloud, Synchronized, Federated)

---

## 🔑 Key Concepts (Must Know)

Microsoft 365 supports three identity models:

1. Cloud Identity  
2. Synchronized Identity  
3. Federated Identity  

👉 Choosing the right model depends on:
- organisation size  
- infrastructure  
- security requirements  

---

## ☁️ 1. Cloud Identity

### What it is

- User exists ONLY in Microsoft Entra ID  
- No connection to on-premises Active Directory  

---

### Key Characteristics

- Managed entirely in the cloud  
- Separate credentials from on-prem (if it exists)  
- Created in Microsoft 365 Admin Center  

---

### Best For

- Small organisations  
- Cloud-only environments  
- No on-prem Active Directory  

---

### Benefits

- Simple setup  
- No infrastructure required  
- Easy to manage  

---

### Limitations

- No integration with on-prem systems  
- Users manage separate credentials  

---

👉 Real-world:
Startups or small companies using only Microsoft 365

---

## 🔄 2. Synchronized Identity (MOST COMMON)

### What it is

- User exists in:
  - On-prem AD  
  - Microsoft Entra ID  

- Identities are synced  

---

### Tools Used

- Microsoft Entra Connect Sync  
- Microsoft Entra Cloud Sync  

---

### Key Characteristics

- On-prem AD = source of truth  
- Changes sync to cloud  
- Limited sync back from cloud  

---

### Authentication Options

#### Cloud Authentication (default)
- User signs in via Microsoft 365  

#### Pass-Through Authentication (PTA)
- Authenticates directly against on-prem AD  

---

### Best For

- Organisations with existing Active Directory  
- Hybrid environments  

---

### Benefits

- Single identity across environments  
- Centralised user management  
- Easier transition to cloud  

---

### Limitations

- Requires sync setup  
- Dependency on sync tools  

---

👉 Real-world:
Most enterprises use this model

---

## 🔐 3. Federated Identity

### What it is

- Authentication handled by external Identity Provider (IdP)  
- Example: AD FS  

---

### How it Works

1. User tries to access Microsoft 365  
2. Redirected to IdP  
3. IdP authenticates user  
4. Token sent back to Microsoft 365  

---

### Key Characteristics

- Requires trust relationship  
- Uses tokens and claims  
- Authentication NOT done in Microsoft 365  

---

### Best For

- Organisations needing advanced authentication  
- Custom login requirements (e.g. smart cards)  
- Centralised authentication control  

---

### Benefits

- True Single Sign-On (SSO)  
- Uses on-prem policies  
- Flexible authentication options  

---

### Limitations

- Complex setup (AD FS required)  
- Dependency on on-prem infrastructure  
- If AD FS is down → users cannot log in  

---

👉 Real-world:
Large enterprises with strict security policies

---

## 🔗 Key Comparison

| Feature | Cloud | Synchronized | Federated |
|--------|------|-------------|----------|
| Identity location | Cloud only | On-prem + Cloud | On-prem + Cloud |
| Authentication | Cloud | Cloud or PTA | External IdP |
| Complexity | Low | Medium | High |
| Best for | Small orgs | Hybrid orgs | Enterprise security |

---

## 🧠 Choosing the Right Model

### Cloud Identity
- No on-prem infrastructure  
- Simple setup  

---

### Synchronized Identity
- Hybrid environments  
- Most common choice  

---

### Federated Identity
- Advanced security needs  
- SSO and custom authentication  

---

## 💼 Real-Life IT Tasks

- setting up Azure AD Connect  
- troubleshooting sync issues  
- managing user accounts in AD  
- configuring Pass-Through Authentication  
- supporting SSO issues  
- maintaining AD FS (if used)  

---

## ⚠️ Common Mistakes

- choosing federated identity unnecessarily  
- not understanding sync vs auth differences  
- relying on on-prem infrastructure without redundancy  
- poor planning for hybrid environments  

---

## 🔥 Interview Questions

### Q1: What are the three identity models in Microsoft 365?

👉 Answer:
Cloud identity, synchronized identity, and federated identity.

---

### Q2: What is the most commonly used identity model?

👉 Answer:
Synchronized identity.

---

### Q3: What is the difference between synchronized and federated identity?

👉 Answer:
Synchronized identities sync user accounts but typically authenticate in the cloud, while federated identities authenticate using an external identity provider like AD FS.

---

### Q4: What is Pass-Through Authentication?

👉 Answer:
An authentication method where user credentials are validated directly against on-prem Active Directory instead of the cloud.

---

### Q5: What is the main benefit of federated identity?

👉 Answer:
Single Sign-On (SSO) using on-prem authentication systems.

---

## 🧠 Summary

- Cloud = simple, cloud-only  
- Sync = hybrid, most common  
- Federated = advanced, SSO  

👉 Identity model choice = foundation of your entire M365 environment
