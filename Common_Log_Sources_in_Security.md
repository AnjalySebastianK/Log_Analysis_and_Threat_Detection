# Common Log Sources in Security

## Windows Logs
- **Location**: Event Viewer (`eventvwr.msc`)
- **Types of Logs**:
  - **System Logs** → Hardware events, driver issues, OS errors.
  - **Application Logs** → Events from installed applications.
  - **Security Logs** → Authentication attempts, privilege use, access control.
- **SOC Use**:
  - Detect failed logins, privilege escalation, malware execution.
  - Investigate system crashes or suspicious service activity.

---

## Linux Logs
- **Location**: `/var/log/` directory.
- **Key Files**:
  - `/var/log/auth.log` → Authentication events (Debian/Ubuntu).
  - `/var/log/secure` → Authentication events (RedHat/CentOS).
  - `/var/log/syslog` → General system activity.
  - `/var/log/messages` → Kernel and daemon logs.
- **SOC Use**:
  - Track SSH login attempts.
  - Monitor sudo usage and privilege escalation.
  - Detect system instability or unauthorized changes.

---

## Firewall Logs
- **Purpose**: Record traffic allowed/blocked by firewall rules.
- **Contents**:
  - Source and destination IP addresses.
  - Ports and protocols used.
  - Action taken (allowed/denied).
- **SOC Use**:
  - Detect port scanning and brute force attempts.
  - Identify suspicious outbound connections (possible data exfiltration).
  - Monitor policy violations and misconfigurations.

---

## Authentication Logs
- **Purpose**: Track user login and identity verification events.
- **Examples**:
  - Active Directory logs (Windows).
  - `/var/log/auth.log` or `/var/log/secure` (Linux).
  - SSO provider logs (Okta, Azure AD).
- **SOC Use**:
  - Detect brute force attacks.
  - Identify compromised accounts.
  - Monitor privilege escalation and insider misuse.

---

## Application Logs
- **Purpose**: Capture events from software, web apps, APIs, and services.
- **Examples**:
  - Web server logs (Apache, Nginx).
  - API request/response logs.
  - Application error logs.
  - Cloud service logs (AWS CloudTrail, Azure Monitor).
- **SOC Use**:
  - Detect web attacks (SQL injection, XSS, CSRF).
  - Monitor API abuse or misuse.
  - Debug application failures and track user actions.

---

# Summary
- **Windows Logs** → OS and application events.
- **Linux Logs** → System, authentication, and kernel activity.
- **Firewall Logs** → Traffic control and network security.
- **Authentication Logs** → User identity and access tracking.
- **Application Logs** → App behavior, errors, and web activity.

Together, these sources provide **complete visibility** for SOC analysts to detect, investigate, and respond to threats.
