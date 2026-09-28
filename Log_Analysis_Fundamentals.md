# Log Analysis Fundamentals

## Event Review
- **Definition**: Systematic examination of logs to identify relevant events.
- **Purpose**:
  - Validate normal vs abnormal activities.
  - Spot anomalies such as failed logins or unusual traffic.
- **SOC Use**:
  - Analysts review logs daily to filter noise and highlight suspicious entries.
  - Helps in triaging alerts and prioritizing investigations.

---

## Timeline Reconstruction
- **Definition**: Building a chronological sequence of events from logs.
- **Purpose**:
  - Understand attacker movement step by step.
  - Correlate events across multiple systems (endpoint, firewall, identity).
- **SOC Use**:
  - Reconstruct how a breach occurred (initial access → privilege escalation → data exfiltration).
  - Provide evidence for forensic investigations and incident reports.

---

## Pattern Recognition
- **Definition**: Identifying recurring behaviors or anomalies in logs.
- **Examples**:
  - Multiple failed logins followed by a successful one → brute force attack.
  - Repeated access to sensitive files → insider threat.
  - Consistent outbound traffic at odd hours → data exfiltration.
- **SOC Use**:
  - Detect hidden threats that blend into normal activity.
  - Train detection rules and SIEM correlation logic.

---

## Suspicious Activities
- **Definition**: Log entries that indicate potential malicious behavior.
- **Examples**:
  - Login from unusual geographic location.
  - Privilege escalation without justification.
  - Disabled security controls (antivirus, firewall).
  - Access to critical resources outside business hours.
- **SOC Use**:
  - Flag suspicious activities for deeper investigation.
  - Reduce false positives by correlating with context.

---

## Investigation Workflows
- **Definition**: Structured process analysts follow when analyzing logs.
- **Steps**:
  1. **Collect** → Gather logs from multiple sources (Windows, Linux, firewall, cloud).
  2. **Filter** → Remove noise and irrelevant entries.
  3. **Correlate** → Link related events across systems.
  4. **Analyze** → Identify root cause and attacker techniques.
  5. **Document** → Record findings for incident response and compliance.
- **SOC Use**:
  - Ensures consistency in investigations.
  - Provides clear evidence trail for management and legal teams.
  - Supports faster containment and remediation.

---

# Key Takeaways
- **Event Review** → Spot anomalies in raw logs.  
- **Timeline Reconstruction** → Build attacker’s step-by-step path.  
- **Pattern Recognition** → Identify recurring malicious behaviors.  
- **Suspicious Activities** → Highlight potential threats.  
- **Investigation Workflows** → Structured process for SOC analysts.  
 
Together, these practices make log analysis a **powerful tool for detection, investigation, and response** in cybersecurity.
