---
title: "Veeam Job Actions"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/veeam_job_actions.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Veeam Job Actions


This step allows you to perform the following job actions required to support plans: enable, disable, start and stop. For example, this step can be useful if you need to disable existing jobs that use storage snapshots in Veeam Backup & Replication.

|  |
| --- |
| Note |
| Orchestrator can recover machines protected by backup and replication jobs only. |

You can override the following parameters for the Veeam Job Actions step:

Veeam Job Actions

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | No |
| Wait for Job to Complete | Defines whether Orchestrator will wait for the action to complete before proceeding to the next step. | Yes |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 600 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 3 |
| Job action | Action to perform on the job. | Enable |
| Job Name | Name of the job to perform actions on. | — |


