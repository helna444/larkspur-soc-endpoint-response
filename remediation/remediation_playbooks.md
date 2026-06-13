# Remediation Playbooks

## Playbook 1: Disable Suspicious Linux User

Trigger condition:

A suspicious or compromised local Linux account is suspected.

Action:

```bash
sudo usermod -L testuser
