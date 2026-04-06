---
title: "Register Replica VM (Storage)"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/register_vm.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Register Replica VM (Storage)


This step registers the selected VM on a host from a storage recovery location, changes the IP address configuration of the VM, applies the mapping specified for the location, and then powers the VM on.

|  |
| --- |
| Note |
| Before powering a recovered VM on, Orchestrator removes all unused swap (.VSWP) files from the default VM directory. If a custom location is used to store swap files, Orchestrator will not be able to remove them. |

You can override the following parameters for the Register Replica VM (Storage) step:

Register Replica VM (Storage)

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for VM recovery.  If you mark the step as Critical, its failure for a VM from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes (not editable) |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 600 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 2 |


