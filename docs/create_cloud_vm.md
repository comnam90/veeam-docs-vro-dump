---
title: "Restore to Azure"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/create_cloud_vm.html"
last_updated: "12/17/2025"
product_version: "13.0.0.1167"
---

# Restore to Azure


This step restores the selected machine from a vSphere or Veeam agent backup to the Microsoft Azure recovery location specified for the plan.

You can override the following parameters for the Restore to Azure step:

Restore to Azure

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Restored VM Name | Name under which the machine will be recovered and registered. | [%source\_machine\_name%](parameter_variables.md) |
| Public IP | Defines whether a public IP address will be assigned to the recovered VM. | No |
| VM Configuration | Defines the VM configuration to be used to recover machines. | Configuration 1 |
| Restore Timeout (minutes) | Maximum amount of time (in minutes) for the step to execute.  Note: The default parameter value is set to 0, which means that Orchestrator will wait for the step to complete for as long as required. However, if you run the [Halt action](halting_cloud.md) to halt the restore process, Orchestrator will halt the plan immediately, despite the infinite timeout value. | 0 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 2 |


