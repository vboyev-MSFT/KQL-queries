
# KQL Queries Repository

Collection of Microsoft security–focused KQL queries spanning Microsoft 365 Defender, Microsoft Sentinel, Azure Resource Graph (ARG), Defender for Cloud, and related platforms.

Queries emphasize:
- Real‑world detection
- Threat hunting
- Posture visibility
- Operational insight

This repository includes:
- Query Index
- Security Domain Index
- MITRE ATT&CK Tactic Index
- Data Source Index
- Use Case Index

---
## Repository Structure
Queries are organized by product area and scenario:
- **MDE** – Microsoft Defender for Endpoint
- **MDC / ASC** – Microsoft Defender for Cloud
- **M365 Defender / AH** – Advanced Hunting queries
- **MDI** – Microsoft Defender for Identity
- **AAD** – Identity / directory–based detections
- **ARG** – Azure Resource Graph queries
- **Initiatives** – Special collections and benchmark‑aligned queries

---
## Query Index
### Microsoft Defender for Endpoint (MDE)
| Query | Data Source | Use Case |
|-------|-------------|----------|
| QuickScan Completion | DeviceEvents | Validate AV quick scan outcomes |
| Failed Logon from Public IPs | DeviceLogonEvents | Detect suspicious remote logons |
| PowerShell Downloads | DeviceProcessEvents | Detect script‑based execution |
| USB Drive Mounts | DeviceEvents | Monitor removable media |
| USB File Copies | DeviceFileEvents | Spot possible data exfiltration |
| EDR Block Mode Events | DeviceEvents | Identify Defender EDR blocks |
| Screenshot Capture Events | DeviceEvents | Identify data collection attempts |

### Microsoft Defender for Cloud (MDC / ASC)
| Query | Data Source | Use Case |
|-------|-------------|----------|
| ASC All Alerts | SecurityAlert | Cloud‑wide alert visibility |
| Pricing / Plan Tier Query | ResourceGraphResources | License / tier mapping |
| Subscription Tier Mapping | ResourceGraphResources | Defender for Cloud coverage overview |

### Microsoft Defender for Identity (MDI)
| Query | Data Source | Use Case |
|-------|-------------|----------|
| LDAP Binds | IdentityDirectoryEvents | Track LDAP authentication activity |
| WMI & PsExec Detection | IdentityDirectoryEvents | Identify lateral movement |

### Azure Resource Graph (ARG)
| Query | Data Source | Use Case |
|-------|-------------|----------|
| VM Extensions Inventory | ResourceGraphResources | Audit extension configuration |
| D4S P1/P2 SKU Inventory | ResourceGraphResources | Subscription SKU mapping |
| VM Communication Reports | ResourceGraphResources | Endpoint‑level network visibility |

### Microsoft 365 Defender – Advanced Hunting
| Query | Use Case |
|-------|-----------|
| MITRE Chart of Alerts | Visualize alerts by tactic |
| Table Size Query | Understand table volume usage |
| Browser URL Access | Web activity analytics |
| QuickScan Health Reports | Endpoint hygiene |

---
## MITRE ATT&CK Tactic Index
### Initial Access
- Public IP logons
- Malicious parent–child process chains (PowerShell, CMD)

### Execution
- PowerShell Downloads
- Parent Process Spawning CMD.EXE

### Persistence
- Local Admin Changes
- Suspicious AAD group or directory role changes

### Privilege Escalation
- Local admin usage
- AAD elevated role assignments

### Defense Evasion
- ASR bypass indicators
- Tamper protection not enabled
- Log4J/NP/CBP alerts

### Credential Access
- LDAP bind anomalies
- Authentication deviations

### Lateral Movement
- WMI / PsExec execution
- Remote command execution

### Collection
- Screenshot capture events
- USB file copying

### Command & Control
- Network Protection blocks
- Suspicious browser activity
- EDR freeze activity

---
## Data Source Index
- DeviceProcessEvents
- DeviceFileEvents
- DeviceNetworkEvents
- DeviceLogonEvents
- EmailEvents
- CloudAppEvents
- IdentityDirectoryEvents
- ResourceGraphResources
- SecurityAlert
- AzureActivity
- AuditLogs

---
## Use Case Index
### Threat Hunting
- Suspicious remote logons
- Script‑based execution (PowerShell)
- WMI / PsExec lateral movement
- Suspicious privilege changes

### Incident Response
- Screenshot capture traces
- USB activity investigation
- Malicious command process trees

### Security Posture & Hygiene
- Defender for Cloud plan tier reporting
- Secure configuration assessment
- Antivirus / EDR health checks

### Inventory & Compliance
- VM extension coverage
- Subscription tier mapping
- Table ingestion volume analysis

### Reporting & Analytics
- MITRE tactic mapping
- Web activity reports
- Endpoint hygiene dashboards

---
## Contributing
When adding a new query, include metadata at top:
```
// Title:
// Description:
// Product:
// Data Source:
// MITRE Tactic:
// Last Updated:
```
Include example outputs when possible.

---
## License
MIT License

