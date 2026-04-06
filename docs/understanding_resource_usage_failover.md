---
title: "How Orchestrator Places VMs During NetApp Storage Failover"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/understanding_resource_usage_failover.html"
last_updated: "10/9/2025"
product_version: "13.0.0.1167"
---

# How Orchestrator Places VMs During NetApp Storage Failover


To fail over VMs to destination storage volumes, Orchestrator performs the following steps:

1. The solution looks through all datastores included in the plan as plan groups.

For each datastore, Orchestrator identifies a storage recovery location that will be used to recover VMs whose disks are stored on this datastore, and mounts the recovered datastore to all hosts added to the storage recovery location as [compute resources](storage_location_compute_resources.md).

|  |
| --- |
| Tip |
| If a datastore is protected by multiple storage systems, Orchestrator takes into account only those systems that are added to storage recovery locations as described in section [Adding Storage Recovery Locations](storage_location_compute_resources.md). This allows you to exclude unnecessary storage systems from the list of locations used to recover VMs. |

If Orchestrator fails to mount any of the recovered datastores to any of the hosts, the plan halts. To learn how to manage halted storage plans, see [Managing Halted Storage Plans](managing_halted_storage_plans.md).

1. To define hosts where the recovered VMs will be registered, Orchestrator performs the following steps:

1. The solution looks through all hosts added to the storage recovery location as compute resources to detect a host that meets the following requirements:

* The host is available.
* The required datastore is mounted to the host.

1. Orchestrator applies the mapping specified in the [network mapping table](storage_location_network_mapping.md) for the storage recovery location to define the required network configuration of the recovered VM.

The solution checks whether the network configuration of the detected host matches the required network configuration:

* If these configurations do not match, Orchestrator goes back to step 2A.
* If these configurations do match, the first processed VM will be registered on this host.

1. When Orchestrator starts processing the next VM, the solution looks through all hosts added to the location as compute resources to detect the next available host.

If Orchestrator detects such a host, this is the host where the VM will be registered. If there are no more available hosts, Orchestrator uses the host detected at step 2B to register the VM.

1. Orchestrator repeats step 2C for all other VMs included in the plan until all the VMs are registered. The order in which the VMs are processed depends on the VM recovery options defined while configuring the plan.

|  |
| --- |
| Note |
| The failure of steps 2A–2D for a VM from a [critical inventory group](configuring_group_settings.md#critical) halts the plan in the following cases:   * If none of the discovered hosts is available. * If none of the hosts has network configuration that matches the required network configuration of the recovered VMs.   To learn how to work with HALTED storage plans, see [Managing Halted Plans](managing_halted_storage_plans.md). |


