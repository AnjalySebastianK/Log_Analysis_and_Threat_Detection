# Understanding Attack Patterns

## Brute-Force Attacks
- **Definition**: Repeated attempts to guess usernames or passwords until successful.
- **Indicators**:
  - Multiple failed login attempts from the same IP.
  - Rapid authentication requests across many accounts.
  - Account lockouts triggered by excessive failures.
- **SOC Response**:
  - Implement account lockout policies.
  - Monitor authentication logs for abnormal login activity.
  - Use MFA to reduce brute-force success rates.

---

## Credential Abuse
- **Definition**: Using stolen or leaked credentials to gain unauthorized access.
- **Indicators**:
  - Successful logins from unusual geographic locations.
  - Privilege escalation without justification.
  - Use of dormant or disabled accounts.
- **SOC Response**:
  - Monitor for impossible travel (logins from distant locations in short time).
  - Detect abnormal role assignments or privilege changes.
  - Enforce credential hygiene (password rotation, MFA).

---

## Malware Execution Indicators
- **Definition**: Signs that malicious software has been executed on a system.
- **Indicators**:
  - Unusual process creation (e.g., `powershell.exe` spawning suspicious scripts).
  - Registry changes disabling security tools.
  - Unexpected outbound connections to unknown IPs/domains.
  - File hash matches with known malware signatures.
- **SOC Response**:
  - Quarantine affected endpoints.
  - Compare suspicious file hashes against threat intelligence feeds.
  - Investigate persistence mechanisms (scheduled tasks, services).

---

## Lateral Movement Awareness
- **Definition**: Attackers moving sideways across systems to expand access.
- **Indicators**:
  - Admin accounts logging into servers they never accessed before.
  - Use of remote execution tools (PsExec, WMI, RDP).
  - Multiple authentication attempts across different hosts.
- **SOC Response**:
  - Monitor for unusual Kerberos ticket usage.
  - Detect workstation-to-many-server authentication patterns.
  - Apply least privilege and tiered admin models.

---

## Data Exfiltration Indicators
- **Definition**: Unauthorized transfer of sensitive data outside the organization.
- **Indicators**:
  - Large outbound traffic volumes at odd hours.
  - Use of uncommon protocols (FTP, SCP) for data transfer.
  - Connections to suspicious external domains.
  - Cloud storage uploads from unauthorized accounts.
- **SOC Response**:
  - Monitor DLP (Data Loss Prevention) alerts.
  - Detect abnormal file access patterns.
  - Block suspicious outbound connections at firewalls.

---

# Key Takeaways
- **Brute-Force Attacks** → Repeated login attempts.  
- **Credential Abuse** → Using stolen identities.  
- **Malware Execution** → Evidence of malicious software running.  
- **Lateral Movement** → Attackers expanding access across systems.  
- **Data Exfiltration** → Unauthorized transfer of sensitive information.  

 Recognizing these attack patterns helps SOC analysts **detect, investigate, and contain threats** before they escalate.
