---
title: "VM Power Actions"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/vm_power_actions.html"
last_updated: "1/8/2026"
product_version: "13.0.0.1167"
---

# VM Power Actions


This step allows you to perform the following VM power actions required to support recovery plans: power on, power off, shutdown, suspend and resume. For example, this step can be useful if you need to power off non-critical VMs in the DR site to free resources required for recovery.

|  |
| --- |
| Important |
| Do not use this step to perform power actions on replica VMs. These actions are automatically performed during the [Process Replica VM](process_replica_vm.md) step execution. |

You can override the following parameters for the VM Power Actions step:

VM Power Actions

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for VM recovery.  If you mark the step as Critical, its failure for a VM from a critical inventory group will halt the plan. | No |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab.  Note: If you set the parameter value to Execute, keep in mind that all actions performed while testing the plan will not be reverted when the test is over. | No |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations.  Note: If you set the parameter value to Execute, the step will perform an action opposite to that specified for the Power Action parameter. For example, if you set the Power Action parameter value to Power On, the step will power off the selected VMs during the Failback and Undo Failover operations. | Yes |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 1 |
| Action | Power action to perform on the VMs. | Power On |
| vCenter Name | Name of the vCenter Server where the VMs are located.  Note: Use separate step instances for each VMware connection. | — |
| VM Names | Names of the VMs to perform power actions on.  Note: To add multiple VMs, use commas. | — |


