---
title: "Verify Exchange Services"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/verify_exchange_services.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Verify Exchange Services


This step verifies that Microsoft Exchange services are running on the recovered VM.

|  |
| --- |
| Important |
| 1. To allow the script to run inside the guest OS of a processed machine, it is required that you have Microsoft PowerShell 3.0, .Net Framework 4.0 and Exchange Server 2013 (or later) installed on each machine for which you enable this step. 2. To allow the script to verify that the services are running on the selected machine, the machine must run Microsoft Windows Server 2008 R2 (or later). |

You can override the following parameters for the Verify Exchange Services step:

Verify Exchange Services

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | No |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 10 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS. | In-Guest OS (not editable) |
| Credentials | Credentials required to gain access to the in-guest OS. | — |
| Exchange Server | Name of the machine where Microsoft Exchange Server runs. | [%vm\_fqdn%](parameter_variables.md) |


