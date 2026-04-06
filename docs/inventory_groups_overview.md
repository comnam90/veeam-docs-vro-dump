---
title: "Inventory Groups"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/inventory_groups_overview.html"
last_updated: "7/25/2025"
product_version: "13.0.0.1167"
---

# Inventory Groups


Inventory groups are sets of virtual or physical machines that are managed by the embedded Veeam ONE server installed on the Orchestrator server.

To create recovery plans, you will use one or more inventory groups that contain objects to recover. The majority of inventory groups are created automatically, based on discovered items such as Veeam Backup & Replication jobs, Veeam agent protection groups, vSphere datastores, vSphere VM tags and Hyper-V custom properties. Unless an inventory group is added to the list of inventory items for at least one scope with the Plan Author or Administrator user role assigned, it will not be available for use in the scope. For more information, see [Managing Inventory Items](managing_inventory_items.md).

Types of Inventory Groups

Inventory groups are the building blocks of recovery plans. These blocks are created and populated using the embedded Veeam ONE server and its Business View engine. Orchestrator automatically creates a group for each of the following:

* Veeam backup job protecting standalone Hyper-V and Azure Local clusters, vSphere VMs and Veeam agents (Windows or Linux).
* Veeam replica or CDP replica job protecting vSphere VMs.
* vSphere datastore containing VMs.
* vSphere datastore containing VMs and backed by a replicating storage system.

* Veeam agent protection group.
* vCenter Server tag for vSphere VMs (the group will be named Category – Tag).
* SCVMM custom property for Hyper-V VMs (the group will be named Custom Property – Value).

|  |
| --- |
| Note |
| You can manage inventory groups manually using [custom categories configured in Veeam ONE Client](categorization_overview.md#customgroups). You can also group VMs based on [categorization data imported from 3rd party software](categorization_overview.md#importgroups). |


