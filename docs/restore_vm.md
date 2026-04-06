---
title: "Restore VM"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/restore_vm.html"
last_updated: "1/21/2026"
product_version: "13.0.0.1167"
---

# Restore VM


This step restores the selected machine to the recovery location specified for the plan.

You can override the following parameters for the Restore VM step:

Restore VM

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Power On VM After Restore | Defines whether the VM will be powered on after the restore operation. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Restore Timeout (minutes) | Maximum amount of time (in minutes) for the step to execute.  Note: The default parameter value is set to 0, which means that Orchestrator will wait for the step to complete for as long as required. However, if you run the [Halt action](halting_restore.md) to halt the restore process, Orchestrator will halt the plan immediately, despite the infinite timeout value. | 0 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 2 |
| Restored VM Name | Name under which the machine will be recovered and registered.  Note: By default, the recovered VM has the name of the source machine. If you want to recover the machine to the same datacenter where the source machine is registered and still resides, it is recommended that you change the parameter value to avoid conflicts. | [%source\_machine\_name%](parameter_variables.md) |


