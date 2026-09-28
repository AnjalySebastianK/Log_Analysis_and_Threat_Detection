# Security Logging Fundamentals

## Importance of Logging
- Logging is the **foundation of security monitoring**.
- Provides **evidence** of system and user activity.
- Helps in **detecting anomalies**, **investigating incidents**, and **ensuring compliance**.
- Without logs, **security teams are blind** to what is happening inside systems and networks.

---

## Log Sources
Logs come from multiple layers of IT infrastructure:
- **Identity Logs** → Authentication, Active Directory, SSO, privilege escalation.
- **Endpoint Logs** → Windows Event Logs, Sysmon, EDR/antivirus.
- **Network Logs** → Firewalls, IDS/IPS, VPN, proxy, NetFlow.
- **Data Logs** → Database access, file servers, cloud storage, DLP.
- **Application Logs** → Web servers, APIs, cloud apps, error logs.

Collecting logs from diverse sources ensures **complete visibility**.

---

## Security Visibility
- Logs provide **visibility into hidden activities**.
- Enable SOC analysts to **spot suspicious behavior**:
  - Failed logins → brute force attempts.
  - Unusual outbound traffic → possible data exfiltration.
  - Privilege escalation → insider threat.
- Visibility ensures **early detection** and **faster response**.

---

## Event Records
- **Event** = Any activity in a system (login, file access, process start).
- **Log** = Recorded evidence of that event.
- Event records include:
  - **Timestamp** → When it happened.
  - **Actor** → Who performed the action.
  - **Action** → What was done.
  - **System** → Where it occurred.
- Event records are the **raw material** for alerts and investigations.

---

## Audit Trails
- **Audit trail** = Chronological sequence of logs/events showing system activity.
- Provides **accountability** → who did what, when, and how.
- Essential for:
  - **Compliance** (ISO, PCI-DSS, HIPAA).
  - **Forensics** (investigating breaches).
  - **Incident response** (tracking attacker movement).
- A strong audit trail ensures **trust and transparency** in security operations.

---

# Summary
- Logging = **eyes and ears** of security.
- Multiple log sources = **complete coverage**.
- Security visibility = **detect threats early**.
- Event records = **detailed evidence**.
- Audit trails = **accountability and compliance**.

