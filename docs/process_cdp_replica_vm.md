---
title: "Process Replica VM (CDP)"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/process_cdp_replica_vm.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Process Replica VM (CDP)


This step performs a number of actions that depend on the plan state:

* Failover — you will fail over from the source VM to the VM replica using the selected restore point. The VM replica will be powered on.
* Failback — you will fail back from the VM replica to the source VM. Changes made to the VM replica will be synchronized with the source VM. The source VM will be powered on.

For more information on other actions that can be performed with by step, see the Veeam Backup & Replication User Guide, section [Failover and Failback for CDP](https://helpcenter.veeam.com/docs/vbr/userguide/cdp_failover_failback.html?ver=13).

You can override the following parameters for the Process Replica VM (CDP) step:

Process Replica VM (CDP)

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for VM recovery.  If you mark the step as Critical, its failure for a VM from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab.  Note: The default parameter value is set to Skip since the current product version does not support testing of CDP replica plans. | Execute (not editable) |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | Execute (not editable) |
| Power On Source VM After Undo | Defines whether the source VM will be powered on during the Undo Failover operation. | Yes |
| Timeout | Timeout (in seconds) used for the Failover and Undo Failover operations. | 1200 |
| Failback Timeout | Timeout (in minutes) used for the Failback operation.  Note: The default parameter value is set to 0, which means that Orchestrator will wait for the step to complete for as long as required. However, if you run the [Halt action](halting_failover_cdp.md) to halt the failback process, Orchestrator will halt the plan immediately, despite the infinite timeout value. | 0 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 2 |


