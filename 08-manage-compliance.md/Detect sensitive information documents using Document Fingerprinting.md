## Document Fingerprinting in Microsoft Purview – Summary

### Overview:
- **Document Fingerprinting** is a Microsoft Purview DLP feature used to:
  - ✅ Detect standard forms/templates
  - ✅ Convert them into **sensitive information types**
  - ✅ Protect documents based on known formats

👉 Focus:
- Identifies documents based on **structure and wording**, not just keywords

---

## Why Use Document Fingerprinting:
- ✅ Protects structured documents (forms/templates)
- ✅ Detects sensitive data in **completed forms**
- ✅ Prevents accidental sharing of standard documents
- ✅ Enhances DLP detection beyond pattern matching  

---

## Common Use Cases:
- Government forms  
- HR employee forms  
- Healthcare (HIPAA forms)  
- Legal documents (contracts, patents)  
- Custom business templates  

---

## How Document Fingerprinting Works:

### Step 1: Upload Template/Form
- Example:
  - Blank patent template  
  - Employee form  

---

### Step 2: Create Fingerprint
- System:
  - Extracts **unique word patterns**
  - Generates:
    - A **hash-based fingerprint (XML)**  

---

### Step 3: Store Fingerprint
- Stored as:
  - Sensitive information type  
- Original document:
  - ❌ NOT stored  
  - ✅ Only hash is retained  

---

### Step 4: Detect Matches
- DLP scans outgoing content:
  - ✅ If document contains same pattern → match  

---

### Key Concept:
👉 Works like fingerprint matching:
- Template = baseline pattern  
- Completed document = variation of pattern  

---

## Example Scenario:

### Step-by-Step:
1. Upload:
   - Blank patent template  
2. Create fingerprint  
3. Create DLP rule using fingerprint  
4. Configure DLP policy:
   - Block external sharing  

---

### Result:
- Any completed patent form:
  - ✅ Detected  
  - 🚫 Blocked (or warned)  

---

## Detection Requirements:

✅ Document must:
- Contain original template text  
- Be text-based  
- Match structure/pattern  

---

❌ Detection fails if:
- File is password protected  
- File contains only images  
- File missing template content  
- File is larger than **10MB**  

---

## Supported Scope:
- ✅ Currently works in:
  - **Exchange Online (email only)**  

---

## Supported File Types:
- Same as:
  - Exchange mail flow rules  
- ❌ Not supported:
  - `.dotx` templates  

---

## How to Create Document Fingerprint (PowerShell):

---

### Step 1: Load File
```powershell
$File = ([System.IO.File]::ReadAllBytes('C:\Path\Template.docx'))
``
