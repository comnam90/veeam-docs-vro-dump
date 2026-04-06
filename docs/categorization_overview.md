---
title: "Grouping and Categorization"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/categorization_overview.html"
last_updated: "11/21/2025"
product_version: "13.0.0.1167"
---

# Grouping and Categorization


|  |
| --- |
| Important |
| Out of the box, Veeam ONE Client comes with the predefined category named B&R Job. This category includes groups of VMs protected by Veeam backup jobs, Veeam replication jobs and Veeam CDP policies that are managed by Veeam Backup & Replication servers connected to Orchestrator. Note that vCenter Servers to which these VMs belong must also be connected to Orchestrator to allow Veeam ONE Client to categorize the VMs.  DO NOT rename or edit the B&R Job category in Veeam ONE Client — this may cause errors when trying to use inventory groups from the category in recovery plans. You can delete this category if you no longer need it. To learn how to delete categories, see the Veeam Recovery Orchestrator Group Management Guide, section [Deleting Categories](https://helpcenter.veeam.com/docs/vro/categorization/delete_categories.html?ver=70). |

Default Categorization

[This section does not apply to machines protected by Veeam agents]

You can group VMs based on vCenter Server tags and SCVMM custom properties that dynamically categorize objects by metadata attached in the vSphere and Hyper-V inventory. VM membership in these groups cannot be edited in the Orchestrator UI — you must modify group properties in Veeam ONE Client, or modify tags and custom properties in the VMware vSphere and Microsoft Hyper-V environment.

To learn how to group VMs using vCenter Server tags and SCVMM custom properties, see the Veeam Recovery Orchestrator Group Management Guide, section [Default Categorization](https://helpcenter.veeam.com/docs/vro/categorization/default.html?ver=13). To learn how to create tag categories and assign tags to infrastructure objects in the vSphere inventory, see [VMware Docs](https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-vcenter-esxi-management/GUID-E8E854DD-AA97-4E0C-8419-CE84F93C4058.html). To learn how to assign custom properties to infrastructure objects in the Hyper-V inventory, see [Microsoft Docs](https://learn.microsoft.com/en-us/powershell/module/virtualmachinemanager/new-sccustomproperty?view=systemcenter-ps-2025).

|  |
| --- |
| Tip |
| After you create a category, edit a category, assign a tag or a custom property to an object in the inventory, the changes may not appear in the Orchestrator UI immediately — the data synchronization process between Orchestrator and Veeam ONE may take more than 3 hours to complete.  You can speed up the data synchronization process using Veeam ONE Reporter installed as part of the embedded Veeam ONE server. To do that:   1. In a web browser, navigate to the Veeam ONE Reporter web address.   The address consists of an FQDN of the Orchestrator server and the website port specified during installation (by default, 1239). Note that Veeam ONE Reporter is available over HTTPS only.  https://<FQDN>:1239/   1. Switch to the Configuration page. 2. Navigate to Data Collection. 3. From the Advanced Actions menu, select Start report data collection. |

Custom Categorization

You can create your own categories and inventory groups using the functionality of Veeam ONE Client. Machine membership in these groups cannot be edited in the Orchestrator UI — you must modify group properties in Veeam ONE Client. You can group machines using the following methods:

* Single-parameter categorization — creates a group for each unique value of the selected property.
* Multiple-condition categorization — allows you to combine multiple conditions that evaluate machine properties for creating groups.
* Categorization with grouping expressions — creates a set of groups and includes machines with matching attributes into these groups.

To learn how to group machines in Veeam ONE Client, see the Veeam Recovery Orchestrator Group Management Guide, sections [Single-Parameter Categorization](https://helpcenter.veeam.com/docs/vro/categorization/single_parameter.html?ver=13), [Multiple-Condition Categorization](https://helpcenter.veeam.com/docs/vro/categorization/multiple_condition.html?ver=13) and [Categorization with Grouping Expressions](https://helpcenter.veeam.com/docs/vro/categorization/grouping_expressions.html?ver=13).

Import-Based Categorization

You can synchronize Business View categorization data with categorization data from 3rd party software. If you have already categorized machines outside Veeam ONE Client, you can describe the categorization model using a .CSV file and then import this file to Veeam ONE Client. Machine membership in these groups cannot be edited in the Orchestrator UI — you must modify categorization data in the .CSV file and then import the file again.

To learn how to import categorization data using .CSV files, see the Veeam Recovery Orchestrator Group Management Guide, section [Import-Based Categorization](https://helpcenter.veeam.com/docs/vro/categorization/import_based.html?ver=13).


