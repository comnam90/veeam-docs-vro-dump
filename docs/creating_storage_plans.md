---
title: "Creating Storage Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/creating_storage_plans.html"
last_updated: "12/26/2025"
product_version: "13.0.0.1167"
---

# Creating Storage Plans


To create a storage plan:

1. Navigate to Recovery Plans.
2. Click Add New Plan.
3. Complete the New Recovery Plan wizard:

1. [Choose a type of the plan](storage_plan_type.md).
2. [Choose a storage vendor for the plan](storage_plan_vendor.md).
3. [Choose a scope for the plan](storage_plan_scope.md).
4. [Specify a plan name and description](storage_plan_name.md).
5. [Specify the target RTO and RPO](storage_plan_rto_rpo.md).
6. [Select a template for plan reports](storage_plan_report_template.md).
7. [Finish working with the wizard](storage_plan_finish.md).

Considerations and Limitations

When you create a storage plan, keep in mind the following:

* Since Orchestrator orchestrates storage failover at the volume level, all VMs that belong to a specific datastore must be processed as part of the same storage plan.
* If a VM that you want to fail over stores its disk files on multiple datastores, make sure to include in the plan all inventory groups related to these datastores. Also, make sure to include the group with the .VMX file into the plan first, before the groups with .VMDK files.
* If the VMs that you want to fail over belong to a datastore in a VMware Storage DRS cluster, make sure to include in the plan all inventory groups related to this cluster.
* Failover to the same VMware vSphere datacenter where the source VMs reside is not supported.
* Failover of VMs that store disks on volumes protected using SnapVault is not supported.
* Failover of VMs with RDM disks is not supported.
* For datastores connected through the NFSv4.1 protocol, Orchestrator supports failover to a recovery location only in the case that target hosts included in the location have the NFSv3 export policy enabled (since the recovered datastores will be mounted to the hosts through NFSv3). For datastores connected through other protocols, no limitations apply.
* If the LUN ID of a datastore where the selected inventory groups belong is greater than 256, Orchestrator may not be able to orchestrate storage failover properly. If the LUN ID is greater than 256, make sure that your equipment supports this ID.
* For Orchestrator to be able to recover a VM correctly, the VM must have VMware Tools installed. The presence of VMware Tools is checked automatically on the vCenter Server side — for both Windows-based and Linux-based VMs. To know how to install and upgrade VMware Tools in vSphere, see [this VMware KB article](https://kb.vmware.com/s/article/2004754).


