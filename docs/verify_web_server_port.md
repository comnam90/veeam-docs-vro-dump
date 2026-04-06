---
title: "Verify Web Server Port"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/verify_web_server_port.html"
last_updated: "1/8/2026"
product_version: "13.0.0.1167"
---

# Verify Web Server Port


This step verifies the port used to connect to the recovered VM with the Web Server role.

You can override the following parameters for the Verify Web Server Port step:

Verify Web Server Port

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | No |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 10 |
| Port Number | Port number to check for access to the Web Service. | 80 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS. | Veeam backup server (not editable) |
| Server | Name of the server to check.  Note: The DNS/NetBIOS name or IPv4 address should be used. | [%current\_vm\_ip\_list%](parameter_variables.md) |


