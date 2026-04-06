---
title: "How Orchestrator Manages HPE Storage Failover"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/orchestrating_storage_failover_hpe.html"
last_updated: "9/29/2025"
product_version: "13.0.0.1167"
---

# How Orchestrator Manages HPE Storage Failover


Orchestrator orchestrates storage failover in the following way when running an HPE storage plan:

1. Before Orchestrator starts processing inventory groups included in the plan, it performs a number of pre-plan steps to prepare the failover environment:

1. Orchestrator runs the VM Control step to shut down source VMs running in the production vCenter Server. To answer VM questions that appear while shutting the VMs down, Orchestrator applies default answers specified in the [vCenter Server settings](https://docs.vmware.com/en/VMware-vSphere/6.7/com.vmware.vsphere.vm_admin.doc/GUID-50FCD2F8-FC99-4AE1-B839-1AC47BF884DC.html).

The VM Control step has a preconfigured timeout parameter that defines the exact amount of time for the step to execute. If the step execution time exceeds the defined parameter value, Orchestrator powers the source VMs off.

1. Orchestrator runs the Storage Failover step. It stops the remote copy group, performs failover on the remote copy group, mounts the secondary volumes to the target vCenter Server, and then mounts the recovered datastores to all hosts in the required storage recovery location.

For more information on the way Orchestrator identifies storage recovery locations required to recover datastores, see [How Orchestrator Places VMs During Storage Failover](understanding_resource_usage_failover_hpe.md#datastores).

1. When processing inventory groups, Orchestrator registers target VMs on hosts in the disaster recovery site, and then powers the VMs on.

For more information on the way Orchestrator defines hosts where recovered VMs will be registered, see [How Orchestrator Places VMs During Storage Failover](understanding_resource_usage_failover_hpe.md#hosts).

1. After Orchestrator finishes processing inventory groups, it performs a number of post-plan steps to finalize the storage failover process:

1. Orchestrator runs the Unregister Source VMs step to unregister source VMs from hosts in the production site.
2. Orchestrator runs the Unmount Source Datastores step to unmount the source volumes from the source vCenter Server.

|  |
| --- |
| Note |
| When Orchestrator orchestrates storage failover, it handles specific internal elements — protection groups and storage items:   * A protection group is an object protected by storage replication. In terms of HPE, it is a storage volume, either primary or secondary. * A storage item is an object that can be connected to the target vCenter Server as a storage device to create a datastore. In terms of HPE, it is a volume or a LUN.   Protection groups and storage items were introduced into Orchestrator to exclusively support the storage failover process. That is why the Orchestrator UI does not show these elements, but you may come across them in some reports and log entries. |


