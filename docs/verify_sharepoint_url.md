---
title: "Verify SharePoint URL"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/verify_sharepoint_url.html"
last_updated: "1/8/2026"
product_version: "13.0.0.1167"
---

# Verify SharePoint URL


This step verifies the SharePoint Server accessibility.

|  |
| --- |
| Important |
| 1. To allow the script to run inside the guest OS of a processed machine, it is required that you have Microsoft PowerShell 3.0, .Net Framework 4.0 and SharePoint 2013 (or later) installed on each machine for which you enable this step. 2. To allow the script to verify the SharePoint Server accessibility, the server must run Microsoft Windows Server 2008 R2 (or later). 3. The account used to run the script must be assigned the SharePoint\_Shell\_Access role and must be a member of the WSS\_ADMIN\_WPG group on each processed machine. |

You can override the following parameters for the Verify SharePoint URL step:

Verify SharePoint URL

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | No |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 10 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS. | In-Guest OS (not editable) |
| SharePoint URL | Name of the SharePoint Server to check. | — |
| Credentials | Credentials required to gain access to the in-guest OS. | — |


