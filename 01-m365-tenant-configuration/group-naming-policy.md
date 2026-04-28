# Microsoft 365 Group Naming Policy (Quick Notes)

---

## 🔑 Key Points

- Enforces **consistent group naming**
- Applies to:
  - Teams
  - Outlook
  - SharePoint
  - Planner
- Applies when:
  - Creating groups
  - Editing group name or alias

---

## ⚠️ Scope

- Applies ONLY to **Microsoft 365 Groups**
- ❌ Does NOT apply to:
  - Distribution groups

---

## 🧩 Naming Policy Features

### 1. Prefix & Suffix

Adds structure to group names

Example:
GRP_Marketing_UK

Can use:
- Fixed text → "GRP"
- User attributes → [Department], [Country]

Example:
GRP_[GroupName]_[Department]

---

### 2. Blocked Words

Prevents users from using sensitive words

Examples:
- CEO
- Payroll
- HR

---

## ⚠️ Licensing

- Requires Microsoft Entra ID P1 (or higher)
- Must cover all users in groups

---

## 🧠 Supported Attributes

- [Department]
- [Company]
- [Office]
- [CountryOrRegion]
- [Title]

---

## ⚠️ Limitations

- Max prefix/suffix length: 53 characters
- Max group name length: 264 characters
- No extension/custom attributes
- No substring matching for blocked words

---

## 💼 Real Work Scenarios

- Standardise naming across Teams and SharePoint
- Identify group purpose quickly (e.g. Dept, Region)
- Prevent users creating sensitive groups (e.g. "CEO Team")
- Improve governance and security

---

## 🎯 Why It Matters (In Real Jobs)

- Keeps environment organised
- Helps IT support quickly identify groups
- Prevents misuse or confusion
- Critical for large organisations

---

## 👑 Admin Override

These roles can bypass policy:

- Global Admin
- User Admin
- Support roles

---

## 🛠️ Where to Configure

Microsoft Entra Admin Center:

Groups → Group settings → Naming policy

---

## 🔥 Interview Questions

Q1: What is a group naming policy?
A: A policy that enforces consistent naming for Microsoft 365 groups

Q2: What does it apply to?
A: Microsoft 365 groups only

Q3: What are the two main features?
A: Prefix/Suffix and Blocked Words

Q4: Why is it important?
A: For governance, organisation, and security

Q5: Can admins bypass it?
A: Yes

---

## 🧠 Summary

- Naming policy = governance + consistency
- Uses prefixes, suffixes, and blocked words
- Helps manage large environments effectively
