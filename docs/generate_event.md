---
title: "Generate Event"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/generate_event.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Generate Event


This step generates events in the Windows event log on the Orchestrator server.

You can override the following parameters for the Generate Event step:

Generate Event

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab.  Note: If you set the parameter value to Execute, keep in mind that all actions performed while testing the plan will not be reverted when the test is over. | No |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Yes |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 60 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 3 |
| Event Text | Event description.  Note: You can use the default text or define [%values%](parameter_variables.md) that will populate during plan execution. | Plan [%plan\_name%](parameter_variables.md) is in state [%plan\_state%](parameter_variables.md) |


