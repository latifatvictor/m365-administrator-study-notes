## Safe Links End-User Experience Summary

- User receives an email containing one or more URLs.
- Email passes through security checks and is delivered to the inbox.
- When the user clicks a link:
  - Safe Links rewrites and redirects it through a Microsoft secure server.
  - The URL is checked against known malicious sites.

### Outcomes:
- ✅ If safe → User is taken to the destination site.
- ❌ If malicious → User is shown a warning page (protective shell).

### Key Behaviors:
- Only malicious links are blocked; safe links in the same email still work.
- Admins can allow users to bypass warnings (optional setting).

---

## Example Scenario:
- Email contains:
  - Malicious link (spamlink.contoso.com)
  - Safe link (bing.com)
- Clicking malicious link → Warning page shown
- Clicking safe link → Opens normally

---

## URL Detonation Experience:
- Combines Safe Links + Safe Attachments
- If a URL points to a downloadable file:
  - File is opened in a secure sandbox (detonated)
  - User sees a "scanning in progress" page

### Outcomes:
- ✅ If safe → User proceeds to content
- ❌ If malicious → Warning page is displayed
