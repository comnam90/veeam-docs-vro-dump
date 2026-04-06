---
title: "Connecting Infrastructure"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/connecting_infrastructure.html"
last_updated: "2/17/2026"
product_version: "13.0.0.1167"
---

# Connecting Infrastructure


If required, you can configure connections to vCenter Servers, SCVMM servers, Hyper-V clusters and NetApp or HPE storage systems.

If you have already connected Veeam Backup & Replication servers in the Initial Configuration wizard, you do not need to connect them again. For more information, see [After You Install](after_you_install.md).

|  |
| --- |
| Note |
| No additional connection is required for recovery to Microsoft Azure as Orchestrator will use the Microsoft Azure compute and storage credentials configured on the connected Veeam Backup & Replication servers. However, if you plan to execute custom scripts inside an Microsoft Azure machine, you must configure a direct connection to this machine as described in section [Connecting Microsoft Azure Servers](connecting_azure_servers.md). |

In This Section

* [Connecting Veeam Backup & Replication Servers](connecting_backup_servers.md)
* [Connecting VMware vSphere Servers](connecting_vsphere_servers.md)
* [Connecting Microsoft Hyper-V Servers](connecting_scvmm_servers.md)
* [Connecting Storage Systems](connecting_storage_systems.md)


