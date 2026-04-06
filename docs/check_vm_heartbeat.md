---
title: "Check VM Heartbeat"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/check_vm_heartbeat.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Check VM Heartbeat


This step checks heartbeat of the recovered VM using VMware Tools. If VMware Tools are not installed, remove this step from the plan.

You can override the following parameters for the Check VM Heartbeat step:

Check VM Heartbeat

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Yes |
| Heartbeat Count | Number of heartbeats to execute. | 4 |
| Heartbeat Poll Time | Amount of time (in seconds) to wait between heartbeats. | 30 |


