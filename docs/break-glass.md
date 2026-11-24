# Emergency Accounts
- Current Microsoft guidance is that emergency accounts use phishing-resistant credentials, specifically a passkey (FIDO2 security key) or certificate-based authentication, not just a long password. You almost certainly do not have a security key. Say so.
- Mandatory MFA applies to these accounts too, with no exception for break-glass. A password-only emergency account cannot actually be used in the emergency it was created for.
- They need to be excluded from Conditional Access policies that would block them, which requires P1 and comes later.
- Their sign-ins should raise an alert, which needs log integration you have not built.
