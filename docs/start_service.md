---
title: "Start Service"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/start_service.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Start Service


This step starts the Windows Service on the processed machine.

|  |
| --- |
| Note |
| For restore plans, this step is not available when restoring VMs to a Microsoft Hyper-V environment. |

You can override the following parameters for the Start Service step:

Start Service

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Yes |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 10 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS. | In-Guest OS (not editable) |
| Credentials | Credentials required to gain access to the in-guest OS. | — |
| Service Name | Name of the service to start.  Note: A short ServiceName must be used. | — |


