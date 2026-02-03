🚀 KQL Queries Repository
A curated collection of Microsoft security‑focused KQL queries, built for use across Microsoft 365 Defender, Microsoft Sentinel, Azure Resource Graph, and related platforms.
This repository provides:

Practical, real‑world KQL for detection, reporting, and investigation
Coverage across multiple security products and data sources
Queries mapped to MITRE ATT&CK tactics where appropriate
Indexed structure to help you find the right query quickly


📁 Repository Structure
/MDE
/MDC
/M365
/AAD
/ARG
/Initiatives

Each folder contains logically grouped KQL queries based on product area or detection scenario.

🧭 Query Index
Below is a structured index of all queries, organized by:

Security Domain
MITRE ATT&CK Tactic
Data Source
Target Use Case


Note: Categorization is based on typical use of each query. Adjust as you refine metadata inside each file.


🔐 1. Security Domain Index
Microsoft Defender for Endpoint (MDE)



































Query NameData SourceUse CaseMDE – QuickScan CompletionDeviceEventsValidate AV quick scan outcomesMDE – Failed Logon From Public IPsDeviceLogonEventsDetect suspicious remote logon attemptsMDE – PowerShell DownloadsDeviceProcessEventsIdentify suspicious PowerShell web activityMDE – USB Drive MountsDeviceEventsTrack removable device insertionMDE – EDR Block Mode ActivityDeviceEventsShow EDR-enforced blocking actions

Microsoft Defender for Cloud (MDC / ASC)

























QueryData SourceUse CaseASC – All AlertsSecurityAlertGlobal visibility into cloud alertsASC – Pricing / Plan Tier QueryResourceGraphResourcesIdentify subscription ASC tiersASC – Subscription Tier QueryResourceGraphResourcesLicensing overview

Microsoft Defender for Identity (MDI)




















QueryData SourceUse CaseLDAP BindsIdentityDirectoryEventsTrack LDAP authentication activityWMI and PsExec UsageIdentityDirectoryEventsDetect lateral movement tools

Azure Resource Graph (ARG)




















QueryData SourceUse CaseVM Extensions InventoryResourceGraphResourcesAudit VM extension deploymentD4S P1/P2 InventoryResourceGraphResourcesSubscription‑level SKU mapping

Microsoft 365 Defender / AH




















QueryData SourceUse CaseMITRE Chart of AlertsM365 Defender datasetsVisualization of alert mappingTable Size QueryAdvanced Hunting tablesStorage optimization / cost insights

🗡 2. MITRE ATT&CK Tactic Index
Initial Access

Failed logon from public IPs (MDE)
Successful logon from public IP (MDE)

Execution

Suspicious PowerShell Downloads (MDE)
Suspicious CMD spawning (MDE – Parent process spawning cmd.exe)

Persistence

Local Admin Changes (MDE)
AAD – Suspicious Group Adds

Privilege Escalation

Local Admin Usage (MDE)
AAD Directory Role Changes

Defense Evasion

ASR Bypass indicators (MDE)
Tamper Not Enabled (MDE – Log4J and NP CBP)

Credential Access

LDAP binds (MDI)
Unusual authentication attempts

Discovery

VM Extensions Inventory (ARG)
Resource Graph – VM Communication Reports

Lateral Movement

PsExec Activity (MDI / MDE)
WMI Exec Activity (MDI)

Collection

Screenshot Capture Events (MDE)
USB File Copy (MDE)

Command & Control

Network Protection Blocks (MDE)
Browser URL Access Query (MDE)

Impact

EDR Freeze Events (MDE)
TVM Exposure Reports


📊 3. Data Source Index
Advanced Hunting

DeviceProcessEvents
DeviceFileEvents
DeviceNetworkEvents
DeviceLogonEvents
EmailEvents
CloudAppEvents
IdentityDirectoryEvents

Azure Resource Graph

ResourceGraphResources

Microsoft Sentinel

SecurityAlert
Heartbeat
AzureActivity

Defender for Cloud Apps

CloudAppEvents

Entra ID / Identity

IdentityDirectoryEvents
AuditLogs


🎯 4. Target Use Case Index
Threat Hunting

PowerShell Downloads
Public IP Logon Attempts
WMI/PsExec Lateral Movement
Suspicious Group Additions

Incident Response

Screenshot Capture
USB Device Investigation
EDR Block Mode Events

Security Posture & Hygiene

ASC Pricing Tier Queries
Defender Antivirus Status
Secure Configuration Assessment

Inventory & Compliance

VM Extension Inventory
Subscription Plan Tier
Table Size / Data Volume Queries

Reporting & Analytics

MITRE Alert Mapping
Browser URL Access Trends
QuickScan Reporting


🛠 Contributing
All contributions welcome — especially improvements to:

tagging (ATT&CK, domain, data source)
query metadata
examples / sample output
documentation

Feel free to submit a PR or open an Issue.

📄 License
MIT License unless specified otherwise.

## ⚠️ Code Disclaimer

The sample queries and scripts in this repository are provided **as-is** without warranty of any kind. They are intended for **educational and reference purposes only** and should be tested thoroughly before use in production environments.

*   Microsoft and the author assume **no liability** for any damages resulting from the use or misuse of this code.
*   By using these samples, you agree that you are responsible for ensuring compliance with your organization’s security policies and standards.

***
