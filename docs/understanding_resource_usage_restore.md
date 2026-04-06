---
title: "How Orchestrator Places VMs During Restore to vSphere"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/understanding_resource_usage_restore.html"
last_updated: "10/10/2025"
product_version: "13.0.0.1167"
---

# How Orchestrator Places VMs During Restore to vSphere


To restore machines included in a restore plan to a recovery location, Orchestrator uses the following algorithm:

1. The solution looks through all hosts added to the location as [compute resources](restore_location_storage_resources.md) to detect the first available host. This is the host where the first processed machine will be registered.
2. Orchestrator applies the mapping specified in the [network mapping table](restore_location_network_mapping.md) for the location to set the required network configuration of the recovered VM.

Orchestrator checks whether the network configuration of the detected host matches the required network configuration. If these configurations do not match, Orchestrator goes back to step 1.

1. In the list of datastores connected to the host as [storage resources](restore_location_storage_resources.md), Orchestrator searches for the first datastore that both is available and has enough capacity. This is the datastore where files of the machine will be stored.

To calculate the datastore capacity and make sure that it has enough space to accommodate the recovered VM, Orchestrator uses the threshold that you specify [when creating or configuring the location](restore_location_recovery_options.md).

When calculating the amount of free space available on a datastore, Orchestrator assumes that the swap file of the processed machine will be restored to this datastore as well. Orchestrator also takes into account that all disk files of the machine will be restored to the same datastore that stores the .VMX file, regardless of whether the source machine stores its disk files on multiple datastores. This may influence the resulting capacity estimation and the way Orchestrator searches for datastores to restore machines.

|  |
| --- |
| Note |
| The failure of steps 1–3 for a machine from a [critical inventory group](configuring_group_settings.md) halts the plan in the following cases:   * If none of the discovered hosts is available, or if none of the hosts has network configuration that matches the required network configuration of the recovered VM. * If none of the discovered datastores is available, or if none of the datastores meets the capacity requirements.   To learn how to work with HALTED restore plans, see [Managing Halted Plans](managing_halted_restore_plans.md). |

1. When Orchestrator starts processing the next machine, the solution looks through all hosts added to the location as compute resources to detect the next available host:

* If Orchestrator detects such a host, this is the host where the machine will be registered.
* If there are no more available hosts, Orchestrator uses the host detected at step 1 to register the machine.

Then Orchestrator goes through steps 2–3 to detect the target network and datastore for the machine.

1. Orchestrator repeats step 4 for all other machines included in the plan until all the machines are restored. The order in which the machines are processed depends on the VM Recovery Options defined [while configuring the plan](configuring_group_settings.md).

If datastores added to the recovery location as storage resources breach the capacity threshold before all the machines are restored, the failure of this step for a machine from a critical group halts the plan. To troubleshoot the issue, configure the location to add more datastores and try running the halted plan again. To learn how to work with HALTED restore plans, see [Managing Halted Plans](managing_halted_restore_plans.md).


