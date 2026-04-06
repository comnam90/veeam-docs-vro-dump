---
title: "Protect VM Group"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/protect_vm_group.html"
last_updated: "12/17/2025"
product_version: "13.0.0.1167"
---

# Protect VM Group


When you [add an inventory group to an existing plan](adding_vm_groups.md), you have an option to run the Protect VM Group step to protect machines included in the plan.

This step creates a new template-based backup or replication job to back up or replicate machines in the specified inventory group as soon as the recovery process completes. Note that for replica plans, the template job will run only after the plan enters the PERMANENT FAILOVER state.

|  |
| --- |
| Important |
| The Veeam Backup & Replication server on which the template backup or replication job has been created must be connected to the vCenter Server that manages target machines. |

You can override the following parameters for the Protect VM Group step:

Protect VM Group

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Skip (not editable) |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 0 |


