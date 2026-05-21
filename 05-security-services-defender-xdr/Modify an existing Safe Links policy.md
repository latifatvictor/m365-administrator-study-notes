# Microsoft Defender for Office 365 – Modify Safe Links Policy Quick Notes

## Modify Existing Safe Links Policy

### Navigation Path
1. Microsoft 365 Admin Center
2. Show All
3. Admin Centers → Security
4. Microsoft Defender Portal
5. Policies & Rules
6. Threat Policies
7. Safe Links
8. Select policy
9. Edit required settings

---

# Important Notes
- Do NOT select the checkbox when opening the policy.
- Policy settings available are the same as during policy creation.

---

# Safe Links Policy Priority

## Priority Rules
- Policies are automatically assigned priorities based on creation order.
- First policy created = Priority 0 (highest priority).
- Lower number = higher priority.

Example:
```text
Priority 0 = Highest
Priority 1 = Next
Priority 4 = Lower
Processing Behaviour
Safe Links processes policies in priority order.
Processing stops after the first matching policy.
No two policies can share the same priority.
Microsoft Defender vs PowerShell
Microsoft Defender XDR
Priority can only be changed AFTER policy creation.
PowerShell
Priority can be assigned DURING rule creation.
Changing priorities may automatically shift other rules.
Key Exam Points
Lower number = higher priority.
Priority 0 is always the highest priority.
First matching policy wins.
Safe Links settings are edited from the policy details pane.
Policies are processed in order of precedence.
