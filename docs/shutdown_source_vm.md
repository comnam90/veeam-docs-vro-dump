---
title: "Shutdown Source VM"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/shutdown_source_vm.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Shutdown Source VM


This step shuts down the selected source VM. It does not affect the recovered VM.

|  |
| --- |
| Note |
| For restore plans, this step is not available when restoring VMs from Hyper-V backups to a Microsoft Hyper-V environment. |

You can override the following parameters for the Shutdown Source VM step:

Shutdown Source VM

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for VM recovery.  If you mark the step as Critical, its failure for a VM from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab.  Note: If you set the parameter value to Execute, keep in mind that all actions performed while testing the plan will not be reverted when the test is over. | No |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | No (not editable) |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 1 |
| Shutdown Action | Defines whether the step will shut down the guest OS of the source VM.  Note: The Shutdown OS option requires VMware Tools to be installed in the guest OS. | Shutdown OS |


