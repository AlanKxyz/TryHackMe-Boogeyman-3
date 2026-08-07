# Boogeyman 3 Incident Analysis

## Overview

This project presents a Digital Forensics and Incident Response (DFIR) investigation of the Boogeyman 3 challenge from TryHackMe.

The objective was to reconstruct a multi-stage attack chain, identify attacker activities, determine persistence mechanisms, analyze Command & Control communication and investigate lateral movement within the environment.

## Tools Used

- Elastic SIEM
- Kibana
- Sysmon
- Windows Event Logs
- MITRE ATT&CK Framework

## Investigation Summary

### Initial Access
- Phishing email delivered a malicious attachment masquerading as a PDF file.
- The payload was executed through `mshta.exe`.

### Persistence
- A scheduled task named `Review` was created.
- Additional persistence mechanisms were identified during incident analysis.

### Command and Control
- Outbound communication established with a remote C2 server.
- Network activity was correlated using Sysmon Event ID 3 logs.

### Privilege Escalation
- UAC bypass performed using `fodhelper.exe`.

### Credential Access
- Credential dumping activity identified after privilege escalation.

### Lateral Movement
- Indicators of movement between systems were discovered during log analysis.

### Impact
- Attacker activity progressed towards ransomware deployment.

## Key Skills Demonstrated

- Incident Response
- Threat Hunting
- SIEM Investigation
- Windows Log Analysis
- Sysmon Analysis
- Network Analysis
- IOC Identification
- MITRE ATT&CK Mapping

## MITRE ATT&CK Techniques

- T1566 - Phishing
- T1059 - Command and Scripting Interpreter
- T1547 - Boot or Logon Autostart Execution
- T1548 - Abuse Elevation Control Mechanism
- T1003 - OS Credential Dumping
- T1021 - Remote Services

## Lessons Learned

This investigation demonstrates the importance of log correlation, endpoint visibility and effective incident response processes when dealing with multi-stage attacks.
