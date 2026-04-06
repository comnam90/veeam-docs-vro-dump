---
title: "Configuring Common Parameters"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/script_common_parameters.html"
last_updated: "1/21/2026"
product_version: "13.0.0.1167"
---

# Configuring Common Parameters


When you [create a custom script step](uploading_scripts.md), you can set a list of default parameters for script execution. Orchestrator already includes a number of out-of-the-box common default parameters that you can modify as described in section [Adding Custom Scripts](uploading_scripts.md).

|  |
| --- |
| Important |
| To allow the script to run inside the guest OS of a processed machine, it is required that you have Microsoft PowerShell 3.0 and .Net Framework 4.0 installed on each machine for which you enable this step. |

Configuring Common Parameters

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Yes |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 600 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 3 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS.  Note: This parameter cannot be changed when restoring VMs to a Microsoft Hyper-V environment. | Veeam backup server |
| Windows Credentials\* | Credentials required to gain access to the in-guest OS.  Note: Applies only if the Script Execution Location parameter value is set to In-Guest OS. | — |

\*This parameter is not required for custom scripts running inside guest OSes of machines included in cloud plans because these scripts are executed under the NT AUTHORITY\SYSTEM account.

To specify credentials that the script will use to run within the guest OS of a processed machine, follow the instructions provided in section [Configuring Windows Credentials Parameter](customizing_credentials.md).


