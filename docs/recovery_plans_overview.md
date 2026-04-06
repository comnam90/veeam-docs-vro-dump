---
title: "Recovery Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/recovery_plans_overview.html"
last_updated: "11/13/2025"
product_version: "13.0.0.1167"
---

# Recovery Plans


Orchestrator uses the failover and data recovery functionality provided by Veeam Backup & Replication to automate recovery actions. In addition, Orchestrator provides vSphere VM recovery orchestration based on replicated storage snapshots created on NetApp and HPE storage systems. For these purposes, Orchestrator offers 5 types of recovery plans:

* [Replica plans](replica_plans_overview.md) — consist of vSphere VMs that should be failed over to replicas.
* [CDP replica plans](cdp_plans_overview.md) — consist of vSphere VMs that should be failed over to continuous data protection (CDP) replicas.
* [Restore plans](restore_plans_overview.md) — consist of vSphere VM, Hyper-V VM or Veeam agent backups that should be recovered to a VMware vSphere or Microsoft Hyper-V environment.

* [Storage plans](storage_plans_overview.md) — consist of VMs that store their files on vSphere datastores backed up by replicating NetApp and HPE storage systems.
* [Cloud plans](cloud_plans_overview.md) — consists of vSphere VM and Veeam agent backups that should be recovered to a Microsoft Azure cloud environment.

Recovery Plans

| Plan Type | Workload Protection | Target Environment |
| Replica | vSphere VM replicas | VMware vSphere |
| CDP Replica | vSphere VM CDP replicas | VMware vSphere |
| Restore | vSphere VM backups | VMware vSphere, Microsoft Hyper-V |
| Veeam agent backups | VMware vSphere |
| Hyper-V VM backups | Microsoft Hyper-V |
| Storage | vSphere VMs | VMware vSphere |
| Cloud | vSphere VM backups | Microsoft Azure |
| Veeam agent backups | Microsoft Azure |


