# Microsoft Defender for Office 365 – Safe Links PowerShell Quick Study Notes

## Safe Links PowerShell Overview
- Safe Links policies and rules are managed separately in PowerShell.
- Policy = Defines actions/settings.
- Rule = Defines recipients, conditions, and priority.

---

# Important Rule
Create:
1. Safe Links POLICY first
2. Safe Links RULE second

Reason:
- Rule must reference an existing policy.

---

# Safe Links PowerShell Cmdlets

## Policy Cmdlets
```powershell
Get-SafeLinksPolicy
New-SafeLinksPolicy
Set-SafeLinksPolicy
Remove-SafeLinksPolicy
Rule Cmdlets
Get-SafeLinksRule
New-SafeLinksRule
Set-SafeLinksRule
Remove-SafeLinksRule
Important PowerShell Facts
Policies and rules are managed separately.
Deleting a policy does NOT delete the rule.
Deleting a rule does NOT delete the policy.
Policies created in PowerShell are NOT visible in Microsoft Defender portal until assigned to a rule.
Create Safe Links Policy Syntax
New-SafeLinksPolicy -Name "<PolicyName>" `
-IsEnabled $true `
-EnableSafeLinksForTeams $true `
-ScanUrls $true `
-DeliverMessageAfterScan $true `
-EnableForInternalSenders $true `
-DoNotAllowClickThrough $true
Important Safe Links Policy Parameters
Parameter	Purpose
IsEnabled	Enables Safe Links
EnableSafeLinksForTeams	Enables Teams protection
ScanUrls	Enables URL scanning
DeliverMessageAfterScan	Waits for scan before delivery
EnableForInternalSenders	Protects internal emails
DoNotAllowClickThrough	Blocks users from bypassing warning pages
DoNotTrackUserClicks	Disables click tracking
DoNotRewriteUrls	Excludes URLs from rewriting
Create Safe Links Rule Syntax
New-SafeLinksRule -Name "<RuleName>" `
-SafeLinksPolicy "<PolicyName>" `
-RecipientDomainIs contoso.com
Rule Purpose
Assigns policy to recipients/domains/groups.
Controls who receives protection.
Safe Links Priority
Priority Rules
Lower number = higher priority
Highest priority = 0
Processing stops after first matching rule
Set Rule Priority
Set-SafeLinksRule -Identity "Marketing Department" -Priority 2
Priority Behaviour

Changing rule priority automatically shifts other rules.

Example:

Priority 2 → 3
Priority 3 → 4
Key Exam Points
Safe Links policies define protection settings.
Safe Links rules define recipients and priority.
Always create policy before rule.
Safe Links supports:
Email
Teams
Office apps
Microsoft recommends:
URL scanning ON
Internal protection ON
Click-through OFF
Real-time scanning ON
