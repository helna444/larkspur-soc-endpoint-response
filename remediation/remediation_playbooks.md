# Remediation Playbooks

## Playbook 1: Disable Suspicious Linux User

Trigger condition:

A suspicious or compromised local Linux account is suspected.

Action:

sudo usermod -L testuser

Verification:

sudo passwd -S testuser

Expected result:

testuser L

Rollback:

sudo usermod -U testuser

## Playbook 2: Block Suspicious Endpoint IP

Trigger condition:

Suspicious communication is identified from endpoint IP address 192.168.70.10.

Action:

sudo ufw deny from 192.168.70.10

Verification:

sudo ufw status numbered

Expected result:

UFW shows an active deny rule for 192.168.70.10.

Rollback:

sudo ufw delete deny from 192.168.70.10
