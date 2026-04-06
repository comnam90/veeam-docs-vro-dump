---
title: "How Orchestrator Places VMs During Restore to Hyper-V"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/understanding_resource_usage_restore_hyperv.html"
last_updated: "10/10/2025"
product_version: "13.0.0.1167"
---

# How Orchestrator Places VMs During Restore to Hyper-V


To restore VMs included in a restore plan to a recovery location, Orchestrator uses the following algorithm:

1. The solution looks through all hosts of the Hyper-V or Azure Local cluster [added to the location](hyperv_location_server.md) to detect the first available host. This is the host where the first processed VM will be registered.
2. Orchestrator applies the mapping specified in the [network mapping table](hyperv_location_network_mapping.md) for the location to set the required network configuration of the recovered VM.

Orchestrator checks whether the network configuration of the detected host matches the required network configuration. If these configurations do not match, Orchestrator recovers the VM without connecting it to any network.

1. In the list of CSV disks connected to the host as [storage resources](hyperv_location_server.md), Orchestrator searches for the first CSV disk that is available. This is the CSV disk where files of the VM will be stored.

|  |
| --- |
| Note |
| The failure of steps 1–3 for a VM from a [critical inventory group](configuring_group_settings.md) halts the plan in the following cases:   * If none of the discovered hosts is available. * If none of the discovered CSV disks is available.   To learn how to work with HALTED restore plans, see [Managing Halted Plans](managing_halted_restore_plans.md). |

1. If the target host selected at step 1 is a part of a Hyper-V or Azure Local failover cluster, the processed VM is registered as a cluster resource — this will allow the VM to fail over to another node in the cluster in case the target host becomes unavailable.
2. When Orchestrator starts processing the next VM, the solution looks through all hosts in the added cluster to detect the next available host:

* If Orchestrator detects such a host, this is the host where the VM will be registered.
* If there are no more available hosts, Orchestrator uses the host detected at step 1 to register the VM.

Then Orchestrator goes through steps 2–3 to detect the target network and CSV for the VM.

1. Orchestrator repeats step 4 for all other VMs included in the plan until all the VMs are restored. The order in which the VMs are processed depends on the VM Recovery Options defined [while configuring the plan](configuring_group_settings.md).


