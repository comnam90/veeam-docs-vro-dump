---
title: "How Orchestrator Places VMs During Cloud Restore"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/understanding_resource_usage_cloud.html"
last_updated: "11/19/2025"
product_version: "13.0.0.1167"
---

# How Orchestrator Places VMs During Cloud Restore


To restore machines included in a cloud plan to a new Microsoft Azure recovery location, Orchestrator uses the following algorithm:

1. Orchestrator checks the connection to the [selected backup server](cloud_location_backup_servers.md) and the availability of the [Microsoft Azure subscription on the server](cloud_location_compute_storage.md#subscription).
2. Orchestrator checks the connections to [all backup repositories](cloud_location_backup_servers.md) that store restore points of all machines added to the plan.

If the list of selected repositories contains a cloud repository, Orchestrator also checks whether the [region specified for the recovery location](cloud_location_compute_storage.md#region) matches the repository region. If the regions do not match, Orchestrator notifies that the recovery process will involve cross-region data transfer.

1. Orchestrator checks whether the [configured backup proxies](cloud_location_backup_servers.md) are connected to the selected Veeam Backup & Replication server.
2. Orchestrator checks whether the [selected resource group](cloud_location_compute_storage.md#resourcegroup) is still present in Microsoft Azure.
3. Orchestrator applies the mapping specified in the [network mapping table](restore_location_network_mapping.md) for the location to set the required network configuration of the first processed machine. Orchestrator also checks whether the network configuration of the source machine matches the required network configuration.

|  |
| --- |
| Note |
| The failure of steps 1–5 for a machine from a [critical inventory group](configuring_group_settings.md#critical) halts the plan in the following cases:   * If the selected Veeam Backup & Replication server is not available. * If the source machine does not have network configuration that matches the required network configuration of the recovered VM. * If the backup repository that stores restore points of the processed machine is not available. * If none of the configured backup proxies is available. * If the selected resource group is not present in Microsoft Azure.   To learn how to work with HALTED cloud plans, see [Managing Halted Plans](managing_halted_cloud_plans.md). |

1. Orchestrator verifies whether the VM configuration specified when [creating the recovery location](cloud_location_compute_storage.md#VMconfig) matches the VM configuration specified when [configuring the plan step parameters](configuring_step_parameters.md). It also checks whether the VM series in the VM configuration is available in the selected region and whether the machine can be restored using these series:

* If the number of machine disks exceeds the maximum number of disks supported for the selected series, the plan halts.
* If the number of CPUs or the amount of RAM required for the recovered VM exceeds the series capacity, Orchestrator displays a warning notifying that the maximum amount of available resources will be used for recovery.

1. Orchestrator repeats steps 5 and 6 for all other machines included in the plan until all the machines are restored. The order in which the machines are processed depends on the VM Recovery Options defined [while configuring the plan](configuring_group_settings.md).


