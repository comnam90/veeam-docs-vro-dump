---
title: "Verify Exchange Mailbox"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/verify_exchange_mailbox.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Verify Exchange Mailbox


This step verifies the Exchange Mail Server accessibility.

|  |
| --- |
| Important |
| 1. To allow the script to run inside the guest OS of a processed machine, it is required that you have Microsoft PowerShell 3.0, .Net Framework 4.0 and Exchange Server 2010 (or later) installed on each machine for which you enable this step. 2. To allow the script to gain access to the Exchange Mail Server to verify the Exchange mailbox, the Exchange Server must run Microsoft Exchange Web Services Managed API 2.1 (or later). The script will use the EWS Managed API to access the server. 3. To allow the script to verify the Exchange mailbox, the Exchange Mail Server must run Microsoft Windows Server 2008 R2 (or later). 4. The account used to run the script must have the ApplicationImpersonation permissions on the Exchange Mail Server. However, keep in mind that once you assign these permissions to the account, the Active Directory synchronization process may take up to 15 minutes for one Active Directory Site (and longer if there are multiple AD Sites involved).   After the synchronization process is over, replicate or back up your Lab Group Domain Controller so the account used to test plans also has the permissions. To learn how to manage impersonation rights, see [this CodeTwo KB article](https://www.codetwo.com/kb/how-to-set-impersonation-rights-manually/#ECP). |

You can override the following parameters for the Verify Exchange Mailbox step:

Verify Exchange Mailbox

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | No |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 10 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS. | In-Guest OS (not editable) |
| Windows Credentials | Credentials required to gain access to the in-guest OS. | — |
| Exchange Credentials | Credentials required to gain access to the Exchange mailbox. | — |
| Exchange Server | Name of the machine where the Microsoft Exchange Web Services Managed API runs. | [%vm\_fqdn%](parameter_variables.md) |
| Email Address | Email address of the mailbox to check. | — |


