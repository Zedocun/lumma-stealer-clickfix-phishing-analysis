# MITRE ATT&CK Mapping

| Tactic | Technique | ID | Justification |
|--------|-----------|----|---------------|
| Initial Access | Phishing | T1566 | User received a phishing email impersonating Microsoft |
| Execution | User Execution | T1204 | User interaction led to access to a malicious landing page |
| Defense Evasion | Masquerading | T1036 | The phishing page imitated Microsoft branding and a legitimate Windows update |
| Command and Control | Application Layer Protocol: Web Protocols | T1071.001 | The victim system connected to attacker infrastructure over HTTPS |
| Command and Control / Delivery | Ingress Tool Transfer | T1105 | Browser activity suggests suspicious archive download and processing |

## Notes

This mapping is limited to behaviors actually observed in the available telemetry.

No confirmed evidence was observed for:
- persistence
- credential dumping
- discovery
- lateral movement
- exfiltration
