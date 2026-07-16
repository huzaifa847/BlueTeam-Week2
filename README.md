# Blue Team Defensive Exercise
## Detection Rule / Sigma Rule Writing Module

### Project Overview

This project is an individual Week 2 contribution for SafeX Solutions' Blue Team Defensive Exercise.

The objective of this module is to design, validate, and test Sigma detection rules against Windows Event Logs using Chainsaw forensic analysis tool.

---

## Objectives

- Create Sigma detection rules for security threats.
- Map detections with MITRE ATT&CK techniques.
- Test rules against sample Windows Event Logs.
- Document detection results.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Sigma CLI | Rule validation |
| Chainsaw | EVTX log hunting |
| VS Code | Rule development |
| Git/GitHub | Version control |
| Windows Event Logs | Detection testing |

---

## Sigma Rules Developed

### 1. PowerShell Encoded Command Detection

Purpose:
Detects suspicious PowerShell execution using encoded commands.

MITRE ATT&CK:
T1059.001 - PowerShell

---

### 2. Suspicious Rundll32 Execution

Purpose:
Detects possible abuse of Windows Rundll32 for proxy execution.

MITRE ATT&CK:
T1218.011 - Rundll32

Testing Result:
Successfully detected using Sysmon Event Logs.

---

### 3. Suspicious Regsvr32 Execution

Purpose:
Detects suspicious Regsvr32 proxy execution activity.

MITRE ATT&CK:
T1218.010 - Regsvr32

Testing Result:
Successfully detected using Sysmon Event Logs.

---

## Detection Testing

Testing was performed using:

- Windows Sysmon EVTX files
- Chainsaw hunting engine
- Custom Sigma rules

Final Result:
