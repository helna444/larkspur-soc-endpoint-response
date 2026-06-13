# Detection Use Cases

## Purpose

This file documents the main detection use cases used in the endpoint security lab.

The detections are based on Linux and Windows endpoint activity.

Each detection is mapped to a relevant MITRE ATT&CK technique.

## Detection 1: Linux Sudo Privilege Activity

Log source:

Wazuh Linux security events

Trigger condition:

A user runs sudo or performs privilege-related activity.

MITRE ATT&CK mapping:

T1548 Abuse Elevation Control Mechanism

Severity:

Medium

Reason:

Sudo activity can show possible privilege misuse or suspicious admin activity.

## Detection 2: Linux Authentication Activity

Log source:

Linux authentication logs and Wazuh events

Trigger condition:

Login or authentication activity is observed.

MITRE ATT&CK mapping:

T1078 Valid Accounts

Severity:

Medium

Reason:

Authentication events can show possible misuse of valid accounts.

## Detection 3: Linux Process Execution

Log source:

auditd execve events

Trigger condition:

A command execution event is recorded on the Linux endpoint.

MITRE ATT&CK mapping:

T1059 Command and Scripting Interpreter

Severity:

Medium

Reason:

Process execution logs help show what commands were run on the endpoint.

## Detection 4: Windows PowerShell Activity

Log source:

Windows endpoint evidence

Trigger condition:

PowerShell or script activity is reviewed as suspicious.

MITRE ATT&CK mapping:

T1059.001 PowerShell

Severity:

High

Reason:

PowerShell can be used by attackers to run commands, collect information or execute scripts.

## Detection 5: Windows Account or Configuration Evidence

Log source:

Wazuh Windows endpoint data

Trigger condition:

Local account or configuration risk is reviewed.

MITRE ATT&CK mapping:

T1136 Create Account

Severity:

Medium

Reason:

Local account activity and weak configuration can support persistence or further access.

## Notes

The detections were tested in an isolated lab environment.

No real malware was used.

The detections were created for academic demonstration and would need further tuning in a production environment.
