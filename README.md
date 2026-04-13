# AD-Command-centre
Best assistant for tech and IT people
# EZMO AD Command Center

A fast, modern desktop application built to streamline Active Directory management for Tier 1 Helpdesk operations. It bridges the gap between raw PowerShell scripts and heavy Microsoft RSAT tools, providing a secure, user-friendly interface for daily IT tasks.

## Visuals
*(Drop a screenshot of your Login Screen, Main Dashboard, and Audit Panel here so visitors can immediately see the UI)*
## Core Features

* **Smart Dashboard & User Management:** Look up users instantly via Logon ID or Asset Tag. View health status, last logon, and security group memberships at a glance.
* **1-Click Quick Actions:** * Unlock accounts and toggle enable/disable states.
  * Edit standard profile attributes (Title, Department, Asset Tag, Phone).
  * Secure password resets featuring a mathematically secure, 16-character auto-generator.
* **Automated Provisioning:** Quickly create fully formatted AD accounts, assign them to organizational units (OUs), and enforce "change password at next logon" policies.
* **Advanced Domain Auditing:** Instantly scan the domain for security vulnerabilities and compliance issues, including:
  * Passwords set to "Never Expire" (65536 flag).
  * Unauthorized Privileged Accounts (AdminCount=1).
  * Accounts requiring no password (32 flag).
  * Stale/Inactive accounts (90+ days without a logon).

## Enterprise Capabilities

* **Cryptographic Node-Locked Licensing:** Built-in DRM that binds license keys to a specific machine's Hardware ID (HWID) using HMAC-SHA256 signatures, preventing key sharing.
* **Trial Gating:** Unlicensed instances default to a read-only "Demo Mode" that disables modifications while allowing search and audit capabilities.
* **Seamless Auto-Updater:** Integrates a silent background update engine that fetches version data via JSON, downloads new releases, and executes a temporary batch script to hot-swap the .exe without user friction.

## Tech Stack

* **Language:** Python 3
* **UI Framework:** CustomTkinter (Dark Mode by default)
* **Directory Protocol:** ldap3 (NTLM Authentication)
* **Security & Cryptography:** hmac, hashlib, base64, secrets
* **Packaging:** PyInstaller / auto-py-to-exe
