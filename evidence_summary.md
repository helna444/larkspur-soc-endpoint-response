Evidence Summary

Purpose

This file summarises the main evidence collected for the endpoint security lab. The detailed screenshots are included in the written report and will also be shown during the video demonstration.

Core Evidence Collected

Wazuh dashboard showing endpoint visibility.

Linux endpoint active in Wazuh.

Linux security events visible in Wazuh.

Windows endpoint data visible in Wazuh.

Linux user lock remediation evidence.

UFW IP block remediation evidence.

Docker AI automation evidence.

Evidence Notes

The Linux endpoint was successfully connected to Wazuh and was able to send security events to the SIEM. These events included authentication, sudo and audit-related activity.

The Windows endpoint data was also visible in Wazuh. However, the Windows agent later appeared as disconnected. This was recorded as a lab reliability limitation.

The Linux user lock remediation was verified using the command sudo passwd -S testuser. The output showed that the test user account was locked.

The IP block remediation was verified using the command sudo ufw status numbered. The output showed that a deny rule was created for the suspicious endpoint IP address.

The Docker evidence showed that an alert could be classified as high risk and linked to an allowlisted remediation action.

Limitation

The main limitation was the Windows agent reliability issue. Although Windows endpoint data was visible in Wazuh, the agent later showed a disconnected status. In a production environment, this would need further review of the Wazuh agent service, the agent key, Windows firewall settings and Wazuh manager logs.
