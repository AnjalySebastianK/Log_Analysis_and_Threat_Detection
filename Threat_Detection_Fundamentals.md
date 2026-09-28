# Threat Detection Fundamentals

## Detection Logic
- **Definition**: The rules or conditions that determine when an alert should be triggered.
- **Purpose**:
  - Translate security knowledge into actionable detection rules.
  - Define thresholds (e.g., “10 failed logins in 1 minute”).
- **SOC Use**:
  - SIEM/EDR systems rely on detection logic to filter noise.
  - Helps analysts focus on meaningful events.

---

## Behavioral Indicators
- **Definition**: Signs of malicious activity based on attacker behavior, not just static signatures.
- **Examples**:
  - Unusual PowerShell commands.
  - Lateral movement across multiple hosts.
  - Privilege escalation attempts.
- **SOC Use**:
  - Detect advanced persistent threats (APTs).
  - Identify insider misuse.
  - Provide context beyond simple alerts.

---

## Signature-Based Detection
- **Definition**: Matching known patterns of malicious activity (hashes, IPs, domains).
- **Examples**:
  - Antivirus detecting malware via file hash.
  - IDS flagging known exploit payloads.
- **Strengths**:
  - Fast and accurate for known threats.
- **Weaknesses**:
  - Ineffective against zero-day attacks.
  - Can be bypassed by obfuscation.
- **SOC Use**:
  - First line of defense against common malware.
  - Complements behavioral and anomaly detection.

---

## Anomaly Detection Concepts
- **Definition**: Identifying deviations from normal baseline activity.
- **Examples**:
  - User logging in at 3 AM from a new country.
  - Sudden spike in outbound traffic.
  - Unusual process execution on endpoints.
- **SOC Use**:
  - Detect unknown or novel attacks.
  - Provide early warning of suspicious activity.
- **Challenges**:
  - Requires accurate baselines.
  - Can generate false positives if not tuned.

---

## Detection Workflows
- **Definition**: Structured process for handling detections from initial alert to resolution.
- **Steps**:
  1. **Trigger** → Detection logic fires an alert.
  2. **Triage** → Analyst validates severity and context.
  3. **Investigation** → Correlate logs, IOCs, and behaviors.
  4. **Response** → Contain, eradicate, and recover.
  5. **Feedback** → Improve detection rules and workflows.
- **SOC Use**:
  - Ensures consistency in handling alerts.
  - Reduces false positives and wasted effort.
  - Builds a feedback loop for stronger defenses.

---

# Key Takeaways
- **Detection Logic** → Rules that trigger alerts.  
- **Behavioral Indicators** → Attacker actions and techniques.  
- **Signature-Based Detection** → Known threat patterns.  
- **Anomaly Detection** → Deviations from normal baselines.  
- **Detection Workflows** → Structured response process.  

 Threat detection combines **rules, behaviors, signatures, and anomalies** into workflows that empower SOC teams to identify and respond to attacks effectively.
