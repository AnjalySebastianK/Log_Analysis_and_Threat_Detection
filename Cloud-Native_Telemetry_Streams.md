# Cloud-Native Telemetry Streams

## Control Plane Log Architectures
Cloud platforms generate telemetry streams at the **control plane level** — meaning they record actions taken against cloud resources (not just inside workloads).  
These logs provide **visibility, accountability, and threat detection** across cloud environments.

---

## AWS CloudTrail
- **Purpose**: Records all API calls made in AWS (who did what, when, and from where).
- **Captured Data**:
  - Identity of the caller (IAM user, role, service).
  - API action performed (e.g., `CreateBucket`, `StartInstances`).
  - Timestamp of the request.
  - Source IP and request parameters.
- **SOC Use**:
  - Detect unauthorized access attempts.
  - Investigate resource changes (e.g., security group modifications).
  - Provide audit evidence for compliance.
- **Example Event**:
```
{
"eventTime": "2026-09-28T19:44:00Z",
"eventName": "ConsoleLogin",
"userIdentity": {"type": "IAMUser", "userName": "alice"},
"sourceIPAddress": "203.0.113.25",
"responseElements": {"ConsoleLogin": "Success"}
}
```

---

## AWS GuardDuty
- **Purpose**: Threat detection service that analyzes CloudTrail, VPC Flow Logs, and DNS logs.
- **Capabilities**:
- Detects anomalous API calls (e.g., unusual region usage).
- Identifies compromised IAM credentials.
- Flags malicious network activity (e.g., communication with known bad IPs).
- **SOC Use**:
- Provides **actionable security findings** without manual correlation.
- Integrates with SIEM/SOAR for automated response.
- **Example Finding**:
- “IAM user executed `ListBuckets` from a Tor exit node.”

---

## Azure Activity Logs
- **Purpose**: Records all control plane operations in Azure (management actions).
- **Captured Data**:
- Resource creation, modification, deletion.
- Role assignments and access changes.
- Service health events.
- **SOC Use**:
- Detect unauthorized resource deployments.
- Monitor privilege escalation in Azure AD.
- Provide compliance evidence for audits.
- **Example Event**:

```
{
"authorization": {"action": "Microsoft.Compute/virtualMachines/start"},
"caller": "bob@contoso.com",
"eventTimestamp": "2026-09-28T19:44:00Z",
"resourceId": "/subscriptions/1234/resourceGroups/demoRG/providers/Microsoft.Compute/virtualMachines/vm01",
"status": "Succeeded"
}
```

---

# Key Takeaways
- **CloudTrail** → API activity logging in AWS.  
- **GuardDuty** → Threat detection using multiple AWS telemetry streams.  
- **Azure Activity Logs** → Control plane visibility for Azure resources.  

Together, these telemetry streams provide **security visibility, compliance assurance, and proactive threat detection** in cloud-native environments.

