---
title: "Check Networks"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/ping_vm_network.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Check Networks


This step pings the selected machine and VMNICs until a stable response is received or timeout exceeds.

You can override the following parameters for the Check Networks step:

Check Networks

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Execute |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Execute |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 600 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 0 |


