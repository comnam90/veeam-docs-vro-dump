---
title: "Send Email"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/send_email.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Send Email


This step sends an email using the configured SMTP server and subscribed email addresses.

|  |
| --- |
| Note |
| For restore plans, this step is not available when restoring VMs from vSphere backups to a Microsoft Hyper-V environment. |

You can override the following parameters for the Send Email step:

Send Email

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab.  Note: If you set the parameter value to Execute, keep in mind that all actions performed while testing the plan will not be reverted when the test is over. | No |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Yes |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 600 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 0 |
| Recipients | Recipients of the email.  Note: To add multiple addresses, use commas. | — |
| Subject | Subject of the email.  Note: You can use the default text, or define [%values%](parameter_variables.md) which will populate during plan execution. | Orchestrator Email notification for [%plan\_name%](parameter_variables.md) |
| Body | Body of the email.  Note: You can use the default text, or define [%values%](parameter_variables.md) which will populate during plan execution. | Plan [%plan\_name%](parameter_variables.md) is in state [%plan\_state%](parameter_variables.md) |


