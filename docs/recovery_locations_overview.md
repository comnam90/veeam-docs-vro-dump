---
title: "Recovery Locations"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/recovery_locations_overview.html"
last_updated: "12/12/2025"
product_version: "13.0.0.1167"
---

# Recovery Locations


Recovery locations consist of resource groups (that is, infrastructure objects such vSphere hosts) used as target locations when orchestrating recovery. Resource groups are managed by the embedded Veeam ONE server installed on the Orchestrator server.

Orchestrator provides 4 types of recovery locations — [VMware Recovery Locations](#vmware), [Microsoft Hyper-V Recovery Locations](#hyperv), [Storage Recovery Locations](#storage) and [Microsoft Azure Recovery Locations](#cloud).

VMware vSphere Recovery Locations

VMware vSphere recovery locations are used to define compute and storage resources in a VMware vSphere environment required when [running restore plans](running_restore.md), [performing replica failback](failover_failback_replica.md) and [CDP failback operations](failover_failback_cdp.md).

Before you run a restore plan or perform a failback operation, you can choose whether to recover machines to the original or to a new location:

* If you want to restore VMs to their original location, you do not need to configure any resources. However, the original VM location does not apply to Veeam agent backups, only to vSphere VM backups.

Orchestrator already includes a built-in recovery location named Original VM Location — if you select this location, Orchestrator will automatically detect the original location of processed VMs and restore the VMs to that location.

You can customize datastore capacity level, set backup copy preference, allow VM recovery across different locations and enable Instant VM Recovery for the location. For more information, see [Configuring Original VM Location](configuring_original_recovery_location.md).

* If you want to restore machines to a different location, you must first categorize vCenter Server resources into VMware vSphere recovery locations.

For more information on working with VMware vSphere recovery locations, see [Adding Recovery Locations](adding_recovery_locations.md), [Configuring Recovery Locations](configuring_recovery_locations.md) and [Managing Inventory Items](managing_inventory_items.md).

Microsoft Hyper-V Recovery Locations

Microsoft Hyper-V recovery locations are used to define cluster and storage resources in a Microsoft Hyper-V environment required when [running restore plans](running_restore.md).

Orchestrator 13 allows you to recover vSphere and Hyper-V VM backups as Hyper-V VMs. For more information on working with Microsoft Hyper-V recovery locations, see [Adding Recovery Locations](adding_recovery_locations.md), [Configuring Recovery Locations](configuring_recovery_locations.md) and [Managing Inventory Items](managing_inventory_items.md).

Storage Recovery Locations

Storage recovery locations are used to define target storage systems and compute resources required when [running storage plans](running_storage_failover.md).

Storage recovery locations are populated with connected storage systems, and with compute resources from connected vCenter Servers — vCenter Server resources are categorized into groups. To learn how to categorize VMs, see [Grouping and Categorization](categorization_overview.md).

For more information on working with storage recovery locations, see [Adding Recovery Locations](adding_recovery_locations.md), [Configuring Recovery Locations](configuring_recovery_locations.md) and [Managing Inventory Items](managing_inventory_items.md).

Microsoft Azure Recovery Locations

Microsoft Azure recovery locations are used to define cloud resources required when [running cloud plans](running_cloud.md).

Orchestrator 13 allows you to recover machines to Microsoft Azure IaaS as VMs. For limitations that may apply for restoring machines to Microsoft Azure, see the Veeam Backup & Replication User Guide, section [Limitations to Restore to Microsoft Azure](https://helpcenter.veeam.com/docs/backup/vsphere/restore_azure_limitations.html).

|  |
| --- |
| Note |
| Restore to Microsoft Azure does not support [Azure Hybrid Benefit](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/hybrid-use-benefit-licensing?WT.mc_id=Portal-Microsoft_Azure_Compute). This means that all machines recovered to Microsoft Azure are deployed as unlicensed VMs. If required, you can apply your on-premises license by enabling the Azure Hybrid Benefit option after recovery, which will allow you to run your Azure VMs at a reduced cost. |

Before creating a Microsoft Azure recovery location, ensure that you have a Microsoft Azure compute account (Azure AD application) added to the Veeam Backup & Replication server. For more information on adding a Microsoft Azure compute account, see the Veeam Backup & Replication User Guide, section [Microsoft Azure Compute Accounts](https://helpcenter.veeam.com/docs/vbr/userguide/restore_azure_accounts.html?ver=13).

For more information on working with Microsoft Azure recovery locations, see [Adding Recovery Locations](adding_recovery_locations.md), [Configuring Recovery Locations](configuring_recovery_locations.md) and [Managing Inventory Items](managing_inventory_items.md).


