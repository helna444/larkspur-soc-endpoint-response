# larkspur-soc-endpoint-response
Endpoint monitoring and automated response lab for Larkspur Retail Group using Wazuh, Linux, Windows and Docker.

# Larkspur SOC Endpoint Response Lab

This repository contains the supporting artefacts for an endpoint security assessment completed for the fictitious company Larkspur Retail Group.

The lab demonstrates endpoint monitoring, SIEM visibility, detection mapping and controlled remediation using a small virtual environment.

## Lab Components

* Wazuh SIEM server
* Linux endpoint
* Windows endpoint
* Docker-based automation evidence layer

## Lab IP Plan

| Component        | Hostname               | IP Address     | Role                                          |
| ---------------- | ---------------------- | -------------- | --------------------------------------------- |
| Wazuh SIEM       | SOC-SIEM-02            | 192.168.70.30  | SIEM manager and dashboard                    |
| Linux endpoint   | LINUX-WAREHOUSE-02     | 192.168.70.20  | Monitored Linux endpoint                      |
| Windows endpoint | WIN-STORE-CLIENT-02    | 192.168.70.10  | Monitored Windows endpoint                    |
| Automation layer | Docker automation node | Local lab node | Alert classification and remediation evidence |

## Main Objectives

* Collect endpoint telemetry in a SIEM.
* Review Linux and Windows endpoint evidence.
* Map detection use cases to MITRE ATT&CK techniques.
* Demonstrate safe remediation playbooks.
* Include rollback steps for each remediation action.

## Key Detections

1. Linux sudo privilege activity.
2. Linux authentication activity.
3. Linux process execution.
4. Windows PowerShell activity.
5. Windows endpoint account or configuration evidence.

## Remediation Playbooks

* Lock a suspicious Linux user.
* Block a suspicious endpoint IP address using UFW.

## Safety Note

This lab was completed in an isolated virtual environment. No real malware, live attacker infrastructure or third-party targets were used.
