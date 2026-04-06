---
title: "Custom Script"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/custom_script.html"
last_updated: "1/8/2026"
product_version: "13.0.0.1167"
---

# Custom Script


If you have [customized your own script](uploading_scripts.md) to be used when running a recovery plan, you can override the following parameters for the Custom Script step:

|  |
| --- |
| Important |
| To allow the script to run inside the guest OS of a processed machine, it is required that you have Microsoft PowerShell 3.0 and .Net Framework 4.0 installed on each machine for which you enable this step. |

Custom Script

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Yes |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 600 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 3 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS.  Note: The script cannot be executed on the in-guest OS when restoring VMs to a Microsoft Hyper-V environment. | Veeam backup server |
| Windows Credentials | Credentials required to gain access to the in-guest OS.  Applies only if the Script Execution Location parameter value is set to In-Guest OS. | — |


