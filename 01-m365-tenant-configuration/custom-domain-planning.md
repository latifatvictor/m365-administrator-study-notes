# Plan Custom Domain in Microsoft 365 (Quick Notes)

---

## 🔑 Key Points

- Custom domain = your company email (e.g. contoso.com instead of contoso.onmicrosoft.com)
- Required for professional branding and email routing

---

## 📌 Planning Considerations

### 1. Multiple Domains
- Add all domains used in the business
- Example:
  - contoso.com (main)
  - contosogroup.com (subsidiary)

---

### 2. Subdomains
- Supported in M365
- Example:
  - sales.contoso.com
  - hr.contoso.com

⚠️ Must add root domain FIRST

---

### 3. Domain Limits
- Up to **900 domains** per tenant

---

### 4. DNS Hosting
- DNS can be hosted:
  - Internally
  - External provider (GoDaddy, Cloudflare, etc.)

---

### 5. DNS Access Required
You MUST be able to create:

- TXT → verification
- MX → email routing
- CNAME → services (Teams, Autodiscover)
- SRV → Skype/Teams
- A record → web services

---

### 6. Partial Configuration (Important)

You don’t have to move everything to Microsoft 365

Example:
- Keep website hosting external
- Move only email to M365

---

### 7. Special Scenarios

- Mergers → multiple domains in one tenant
- Education → separate domains (staff vs students)
- Hybrid environments → partial DNS changes

---

## 💼 Real Work Scenarios

- Company migration from Google Workspace → add domain to M365
- Merger → support multiple email domains in one tenant
- Hybrid setup → email in M365, website hosted elsewhere
- IT support → troubleshooting email flow (MX records issue)

---

## ⚠️ Common Mistakes

- Forgetting to verify domain (TXT record)
- Wrong MX record → emails not delivered
- No DNS access → delays deployment
- Adding subdomain before root domain ❌

---

## 🎯 Why It Matters

- Enables company email (user@company.com)
- Required for Exchange Online
- Impacts Teams, SharePoint, authentication
- Critical for migrations & hybrid setups

---

## 🔥 Interview Questions

Q1: What is a custom domain in Microsoft 365?
A: A domain you own (e.g. contoso.com) used for email and services instead of default onmicrosoft.com

---

Q2: What DNS records are required for Microsoft 365?
A: TXT, MX, CNAME, SRV, A

---

Q3: Can you add multiple domains to a tenant?
A: Yes, up to 900 domains

---

Q4: What is the correct order when adding domains?
A: Root domain first, then subdomains

---

Q5: What happens if MX records are incorrect?
A: Emails will not be delivered properly

---

Q6: Can you use Microsoft 365 without changing all DNS records?
A: Yes, partial configuration is possible

---

## 🧠 Summary

- Plan domains carefully before adding
- Ensure DNS access
- Root domain comes first
- DNS configuration = critical for email & services
