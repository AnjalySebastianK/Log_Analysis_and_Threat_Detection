# Log Correlation Fundamentals

## Multiple Log Sources
- **Definition**: Collecting logs from diverse systems (identity, endpoint, network, application, cloud).
- **Purpose**:
  - Gain a complete picture of activity across the environment.
  - Avoid blind spots by combining different perspectives.
- **SOC Use**:
  - Correlate authentication logs with firewall logs to detect brute force attacks.
  - Link endpoint logs with application logs to confirm malware execution.

---

## Event Relationships
- **Definition**: Connecting related events across different log sources.
- **Examples**:
  - Failed login attempts (authentication logs) followed by successful login (endpoint logs).
  - Firewall alert for suspicious outbound traffic linked to process creation on a server.
- **SOC Use**:
  - Build context around attacker behavior.
  - Reduce false positives by validating events across multiple systems.

---

## Investigation Timelines
- **Definition**: Chronological reconstruction of correlated events.
- **Purpose**:
  - Show attacker’s step-by-step path.
  - Provide forensic evidence for incident reports.
- **SOC Use**:
  - Reconstruct how an intrusion unfolded (initial access → lateral movement → data exfiltration).
  - Identify dwell time and attack progression.

---

## Alert Enrichment
- **Definition**: Adding context to alerts using correlated log data.
- **Examples**:
  - Enriching a failed login alert with geolocation, device type, and user role.
  - Adding file hash reputation data to endpoint alerts.
- **SOC Use**:
  - Helps analysts quickly understand severity and impact.
  - Improves triage efficiency by reducing investigation time.

---

## Threat Visibility
- **Definition**: Enhanced detection capability through correlation.
- **Examples**:
  - Detecting credential abuse by linking identity logs with network traffic.
  - Spotting data exfiltration by correlating DLP alerts with outbound firewall logs.
- **SOC Use**:
  - Provides a holistic view of attacker activity.
  - Enables proactive threat hunting and continuous monitoring.

---

# Key Takeaways
- **Multiple Log Sources** → Broader coverage.  
- **Event Relationships** → Connect clues across systems.  
- **Investigation Timelines** → Reconstruct attacker path.  
- **Alert Enrichment** → Add context for faster triage.  
- **Threat Visibility** → See the full picture of attacks.  

Log correlation transforms raw data into **actionable intelligence**, empowering SOC teams to detect, investigate, and respond effectively.
