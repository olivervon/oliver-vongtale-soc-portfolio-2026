# SOC Analyst Portfolio - Hybrid Active Directory Detection Lab

This repository documents a hands-on SOC analyst learning environment focused on attack simulation, detection engineering, and incident investigation within a hybrid Active Directory infrastructure.

The lab environment was built to simulate realistic attacker behavior and demonstrate how security events can be detected, analyzed, and investigated using Windows Security logs and Microsoft Sentinel.

The project follows a structured SOC workflow from initial compromise to incident investigation.

## Lab Overview

The environment consists of an on-premise Active Directory lab integrated with Azure monitoring capabilities.

Core components:

- Active Directory Domain Environment
- Windows Server infrastructure
- Attack simulation and adversary techniques
- Windows Security log analysis
- Hybrid cloud log ingestion
- Microsoft Sentinel integration
- SOC-style incident investigation

## Environment Architecture

On-Prem Infrastructure

- DC01 – Domain Controller
- SRV01 – Target Server
- SOC.local Active Directory domain

Cloud Integration

- Azure Arc enabled server
- Log Analytics Workspace
- Microsoft Sentinel SIEM
- Azure Monitor Agent log forwarding

This setup enables visibility from endpoint activity to cloud-based detection.

## Repository Structure

### 01 - Lab Setup

Establishment of the Active Directory environment and baseline configuration used throughout the portfolio.

Focus areas:

- Domain deployment
- Server configuration
- Logging preparation
- SOC lab foundation

### 02 - Attack Chain Simulation

Simulation of a complete attacker workflow inside the domain environment.

Attack stages demonstrated:

1. Initial Access – SMB brute force authentication attempts
2. Credential Compromise – Successful authentication
3. Lateral Movement – SMB authentication to SRV01
4. Privilege Escalation – Local administrator access
5. Credential Dumping – LSASS memory extraction

Security events analyzed primarily include:

- Event ID 4625
- Event ID 4624
- Event ID 4688

This phase demonstrates attacker behavior from a defender visibility perspective.

### 03 - Cloud Integration

Extension of on-premise telemetry into Azure.

Implemented components:

- Azure Arc onboarding
- Data Collection Rules
- Windows Security log forwarding
- Microsoft Sentinel integration
- Hybrid monitoring validation

This phase transitions the lab into a hybrid SOC monitoring environment.

### 04 - Incident Investigation

SOC-style investigation of suspicious persistence activity.

Investigation workflow:

- Persistence detection
- Process execution analysis
- User authentication correlation
- Event timeline reconstruction
- MITRE ATT&CK mapping
- Analyst conclusion

Demonstrated investigative events:

- Event ID 4698 – Scheduled Task Creation
- Event ID 4688 – Process Execution
- Event ID 4624 – User Authentication

This phase represents practical Tier-1 SOC investigation methodology.

## Skills Demonstrated

- Windows Security Log Analysis
- Threat Detection and Investigation
- Active Directory Security Monitoring
- Attack Chain Understanding
- MITRE ATT&CK Mapping
- SIEM Log Ingestion
- Microsoft Sentinel Fundamentals
- Incident Analysis Workflow
- Hybrid SOC Monitoring

## Detection Focus

The primary objective of this portfolio is not offensive security, but detection visibility and investigation capability.

All attack simulations are performed to demonstrate how malicious activity appears from a SOC analyst perspective.

## Project Goal

The goal of this project is to demonstrate practical readiness for a SOC Analyst or Security Operations internship (LIA) through structured, evidence-based security investigations.

The lab emphasizes understanding attacker techniques, log correlation, and defensive analysis rather than theoretical exercises.
