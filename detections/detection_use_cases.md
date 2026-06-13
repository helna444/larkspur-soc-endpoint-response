# Detection Use Cases

| Use Case | Log Source | ATT&CK Technique | Trigger Condition | Severity |
|---|---|---|---|---|
| Linux sudo activity | Wazuh Linux events | T1548 | sudo command or privilege activity | Medium |
| Linux authentication activity | Linux auth logs | T1078 | login or authentication activity | Medium |
| Linux process execution | auditd execve | T1059 | command execution event | Medium |
| Windows PowerShell activity | Windows endpoint evidence | T1059.001 | suspicious script or PowerShell activity | High |
| Windows account/configuration evidence | Wazuh Windows data | T1136 | local account or configuration risk | Medium |
