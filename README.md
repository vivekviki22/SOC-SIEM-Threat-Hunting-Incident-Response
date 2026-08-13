# SOC & SIEM Threat Hunting and Incident Response

## Project Overview

This project demonstrates the implementation of a Security Operations Center (SOC) monitoring environment using Wazuh as the Security Information and Event Management (SIEM) platform.

The lab was designed to collect and analyze security telemetry from Windows and Linux endpoints, detect suspicious activity, simulate controlled security events, perform threat hunting, and document incident response procedures.

The project demonstrates a complete SOC workflow:

Log Collection → Detection → Investigation → Threat Hunting → Incident Response

---

## Project Objectives

The primary objectives of this project were to:

- Deploy and configure a centralized SIEM platform.
- Connect Windows and Linux endpoints to Wazuh.
- Collect and normalize endpoint security logs.
- Detect authentication and privilege-related security events.
- Simulate controlled attacks in an isolated lab.
- Investigate alerts using Wazuh Threat Hunting.
- Correlate security events across multiple log sources.
- Document incident response procedures.
- Develop a reusable SOC Incident Response Playbook.

---

## Lab Architecture

The project was implemented in an isolated virtualized cybersecurity lab.

### Main Components

- Wazuh SIEM
- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard
- Windows Server 2025
- Debian Linux
- Kali Linux
- Wazuh Agents
- VirtualBox

### Security Monitoring Workflow

Endpoint Activity  
↓  
Windows / Linux Security Logs  
↓  
Wazuh Agent  
↓  
Wazuh Manager  
↓  
Wazuh Indexer  
↓  
Wazuh Dashboard  
↓  
Threat Detection & Investigation

---

## Technologies and Tools

The following technologies were used during the project:

- Wazuh
- Windows Server 2025
- Debian Linux
- Kali Linux
- VirtualBox
- Windows Event Viewer
- Linux journald
- Linux audit logging
- SSH
- Hydra / Medusa
- Git
- GitHub

---

## Log Collection

Security telemetry was collected from Windows and Linux endpoints.

### Windows

Examples of monitored activity included:

- Authentication events
- Failed logon attempts
- Privileged logons
- Account creation and modification
- Security group changes

### Linux

Linux monitoring included:

- SSH authentication activity
- sudo activity
- system logs
- journal events
- audit events

Collected events were centralized in Wazuh for security monitoring and investigation.

---

## Threat Detection

The project investigated several security-relevant scenarios, including:

- Repeated authentication failures
- SSH authentication activity
- Privileged Windows logons
- Linux sudo-to-root activity
- Account creation and modification
- Local Administrators group changes
- Controlled data-transfer activity

Wazuh detection rules were used to identify and classify relevant security events.

---

## Attack Simulation

Controlled security activities were performed inside the isolated lab environment to generate security telemetry.

Testing included:

- Repeated authentication attempts
- SSH authentication testing
- Privileged-access activity
- Account manipulation
- Administrative group changes
- Controlled data-transfer activity

These simulations were performed only against systems specifically configured for the cybersecurity lab.

---

## Threat Hunting

Wazuh Threat Hunting was used to investigate security events.

Investigation techniques included:

- Filtering by Wazuh rule ID
- Filtering by Windows Event ID
- Reviewing affected agents
- Reviewing user accounts
- Analyzing authentication failures
- Investigating privileged activity
- Correlating timestamps
- Reviewing related security events
- Building event timelines

The objective was to move beyond individual alerts and understand the context surrounding security activity.

---

## Incident Response

Security events were analyzed using a structured incident response lifecycle:

1. Identification
2. Analysis
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

The project also includes a dedicated SOC Incident Response Playbook describing recommended response procedures.

---

## MITRE ATT&CK

Where supported by Wazuh alerts, MITRE ATT&CK mappings were reviewed to provide additional context for detected activity.

An example observed during the project was:

**T1548.003 — Sudo and Sudo Caching**

This technique relates to abuse of sudo privileges for elevated execution on Linux systems.

---

## Repository Structure

SOC-SIEM-Threat-Hunting-Incident-Response/

    Documentation/
        Project documentation and final reports

    Evidence/
        01-SIEM-Deployment/
        02-Log-Collection/
        03-Threat-Detection/
        04-Attack-Simulation/
        05-Threat-Hunting/
        06-Incident-Response/

    Playbook/
        SOC Incident Response Playbook

    LICENSE
    README.md

---

## Project Evidence

Detailed screenshots and supporting evidence are organized into six categories:

### 01 — SIEM Deployment
Evidence of Wazuh deployment, configuration, and endpoint connectivity.

### 02 — Log Collection
Evidence demonstrating centralized Windows and Linux security telemetry.

### 03 — Threat Detection
Evidence of authentication, privilege, account, and security-event detection.

### 04 — Attack Simulation
Evidence generated during controlled cybersecurity testing.

### 05 — Threat Hunting
Evidence demonstrating Wazuh filtering, event analysis, and correlation.

### 06 — Incident Response
Evidence supporting alert identification, investigation, and response analysis.

---

## Key Skills Demonstrated

This project demonstrates practical experience with:

- Security Operations Center workflows
- SIEM deployment
- Wazuh administration
- Endpoint monitoring
- Windows security-event analysis
- Linux security-log analysis
- Authentication monitoring
- Threat detection
- Alert triage
- Threat hunting
- Event correlation
- Incident investigation
- Incident response
- MITRE ATT&CK
- Security documentation
- Technical evidence collection

---

## Key Takeaways

This project demonstrated how centralized logging and SIEM technology can provide visibility across multiple endpoints.

The exercise reinforced the importance of correlating authentication, privilege, account, and endpoint events rather than analyzing alerts independently.

It also demonstrated how threat detection, threat hunting, and incident response work together as part of a SOC investigation workflow.

---

## Disclaimer

This project was completed in a controlled and isolated cybersecurity lab environment for educational purposes.

All attack simulations and security testing were performed only against systems specifically configured for the lab. No unauthorized production or third-party systems were targeted.
