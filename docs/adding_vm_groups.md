---
title: "Adding Inventory Groups"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/adding_vm_groups.html"
last_updated: "12/10/2025"
product_version: "13.0.0.1167"
---

# Adding Inventory Groups


After you create a recovery plan, you must add to this plan inventory groups that contain VMs that you plan to restore:

1. Navigate to Recovery Plans.
2. Select the plan to which you want to add inventory groups and click Manage > Edit.
3. On the Edit Plan page, click Add.
4. In the Add Inventory Group window, choose groups that you want to add to the plan and click Next. For an inventory group to be displayed in the Group list, it must be added to the list of inventory items available for the scope, as described in section [Managing Inventory Items](managing_inventory_items.md).

Note that one restore plan can contain inventory groups of one type only (either vSphere, Veeam Agent or Hyper-V). To recover workloads added to inventory groups of different types, create separate restore plans.

1. In the Group Options window, configure the group settings as described in section [Configuring Group Settings](configuring_group_settings.md).

1. To save changes made to the plan settings, click Apply.

|  |
| --- |
| Important |
| For Orchestrator to be able to recover a machine to a VMware vSphere environment, it is recommended that the machine has VMware Tools installed:   * For VMs recovered from Veeam agent backups, Orchestrator automatically verifies whether VMware Tools are installed on all machines included in a plan when running a readiness check or a DataLab test for the plan. However, this verification is supported for Windows-based machines only. For Linux-based machines, you must perform the verification manually. * For VMs recovered from vSphere backups, the verification is performed automatically on the vCenter Server side — for both Windows-based and Linux-based VMs. To know how to install and upgrade VMware Tools in vSphere, see [this VMware KB article](https://kb.vmware.com/s/article/2004754). |

[![Adding VM Groups to Plan](images/adding_vms_to_plan.webp)](images/adding_vms_to_plan.webp "Adding VM Groups to Plan")


