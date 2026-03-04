\# Threat Scenarios – Microsoft Sentinel SIEM Lab



This document describes the security scenarios investigated in this lab environment using Microsoft Sentinel and Azure Activity logs.



---



\## Scenario 1 – Repeated Failed Administrative Actions

\*\*Detection Query:\*\* `azureactivity\_failures\_threshold.kql`



\### Threat Context

Repeated failed control-plane operations can indicate:



\- Privilege escalation attempts

\- Credential misuse

\- Automated scripts probing permissions

\- Unauthorized access attempts



\### Detection Logic

The detection rule groups failed operations by user within a 5-minute window and triggers if a threshold is exceeded.



---



\## Scenario 2 – Suspicious Administrative Activity Burst

\*\*Hunting Query:\*\* `admin\_burst\_hunt.kql`



\### Threat Context

Large bursts of operations in short time windows may indicate:



\- Malicious automation

\- Compromised credentials

\- Enumeration of Azure resources



\### Investigation Focus

SOC analysts review:



\- caller identity

\- affected resources

\- operation diversity



---



\## Scenario 3 – Resource Deletion Activity

\*\*Hunting Query:\*\* `destructive\_actions\_hunt.kql`



\### Threat Context

Deletion operations may signal:



\- Data destruction attempts

\- Covering attacker tracks

\- Insider misuse



\### Investigation Focus

\- Which resources were deleted

\- Who performed the operation

\- Whether the action was expected



---



\## Scenario 4 – Privilege / Role Changes

\*\*Hunting Query:\*\* `role\_changes\_hunt.kql`



\### Threat Context

Unauthorized role assignments can lead to privilege escalation in cloud environments.



\### Investigation Focus

SOC analysts verify:



\- new role assignments

\- affected identities

\- authorization scope

