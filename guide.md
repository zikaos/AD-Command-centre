EZMO AD Command Center - Tier 1 Quick Reference

1. Connection

DC IP: IP or Hostname of the Domain Controller (e.g., 10.0.0.5 or dc1.corp.local).

Admin User: Your elevated account (DOMAIN\username).

Base Search: Target OU or domain root (DC=corp,DC=local).

Check "Remember settings" to save connection info. Passwords are never cached.

2. User Management (Dashboard)

Search using Logon ID or Office ID (Asset Tag).

Unlock: Clears the lockoutTime attribute.

Disable/Enable: Toggles account status.

Edit Info: Updates Title, Department, Phone, and Asset Tag.

Reset Password: Use Auto-Gen for a secure 16-character string. Check the box to force change at next logon.

View Groups: Lists all security groups the user belongs to.

3. Provisioning

Creates a new user and sets standard attributes.

Select the target OU from the dropdown (pulls dynamically from AD).

Leave both checkboxes ticked to ensure the account is active and forces a password change.

4. Security Audits

Locked Out: Users currently locked out.

Disabled: Standard list of disabled accounts.

Pwd Never Expires: Accounts flagged with 65536. (Fix these per policy).

Privileged Accounts: Accounts with AdminCount=1 (Domain Admins, Enterprise Admins).

No Pwd Required: Accounts flagged with 32. (Critical security risk).

Stale (90+ Days): Active accounts with no logon event in the last 90 days. Target these for license harvesting/cleanup.

5. Licensing / Activation

App defaults to Read-Only (Trial Mode). Quick Actions are disabled.

Go to Activate Premium and copy your Machine ID (HWID).

Email the HWID to EZMO-IT@outlook.com to get your node-locked key.

Note: Keys are motherboard-locked. You cannot share your key with another tech.

6. Common Errors

LDAP Socket Open Error: Cannot reach the DC. Check your network or VPN.

LDAP Bind Error: Bad admin password, or your own admin account is locked.

Reset Rejected: The new password fails the domain complexity GPO, or your DC requires Port 636 (LDAPS) for password changes.
