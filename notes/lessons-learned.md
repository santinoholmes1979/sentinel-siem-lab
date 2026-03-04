\# Lessons Learned (Microsoft Sentinel Lab)



\- Sentinel experience is accessed through the Microsoft Defender portal UI.

\- Azure Activity ingestion may be enabled via Azure Policy Assignment wizard.

\- Validated ingestion by querying AzureActivity and confirming recent rows.

\- Used a temporary “any activity” rule to confirm incident generation, then restored the failure-threshold rule.

