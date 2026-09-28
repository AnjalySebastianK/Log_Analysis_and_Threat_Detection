# Indicators of Compromise (IOCs)

## What are IOCs?
- **Definition**: Forensic evidence that a system has been breached or malicious activity has occurred.
- **Purpose**:
  - Help SOC analysts confirm incidents.
  - Provide clues for threat hunting and investigation.
  - Feed into SIEM/EDR tools for detection and blocking.

---

## Malicious IPs
- **Description**: IP addresses known to be associated with attackers, botnets, or command-and-control (C2) servers.
- **Examples**:
  - Repeated failed login attempts from the same IP.
  - Outbound traffic to blacklisted IP ranges.
- **SOC Use**:
  - Block malicious IPs at firewalls.
  - Detect suspicious connections in network logs.

---

## Malicious Domains
- **Description**: Domains used for phishing, malware distribution, or C2 communication.
- **Examples**:
  - `evil-update.com` serving fake software updates.
  - `phishing-login.net` mimicking legitimate login pages.
- **SOC Use**:
  - Add domains to DNS blocklists.
  - Detect suspicious outbound requests in proxy logs.

---

## Suspicious File Hashes
- **Description**: Unique cryptographic fingerprints (MD5, SHA‑1, SHA‑256) of malicious files.
- **Examples**:
  - Malware executables (`mimikatz.exe`, ransomware payloads).
  - Trojanized installers or scripts.
- **SOC Use**:
  - Compare file hashes against threat intelligence feeds.
  - Detect malware presence on endpoints.

---

## Unauthorized Access Attempts
- **Description**: Evidence of attackers trying to gain or escalate access.
- **Examples**:
  - Multiple failed login attempts (brute force).
  - Privilege escalation via `sudo` or `runas`.
  - Creation of unauthorized user accounts.
- **SOC Use**:
  - Detect compromised credentials.
  - Investigate insider threats.
  - Trigger alerts for suspicious authentication patterns.

---

## Threat Indicators
- **Description**: Broader set of clues pointing to malicious activity.
- **Examples**:
  - Registry changes disabling security tools.
  - Unusual PowerShell or Bash commands.
  - Data exfiltration logs showing large outbound transfers.
- **SOC Use**:
  - Correlate across multiple sources (endpoint, network, identity).
  - Build detection rules in SIEM/XDR platforms.
  - Support forensic investigations.

---

# Key Takeaways
- **Malicious IPs** → Detect hostile network sources.  
- **Malicious Domains** → Spot phishing and malware distribution.  
- **Suspicious File Hashes** → Identify known malware.  
- **Unauthorized Access Attempts** → Reveal compromised accounts.  
- **Threat Indicators** → Provide context for deeper investigations.  

IOCs are the **footprints left behind after an attack** — they help analysts confirm, investigate, and respond to security incidents.
