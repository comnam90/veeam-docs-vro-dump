---
title: "Managing Recovery Locations"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/managing_recovery_locations.html"
last_updated: "7/29/2025"
product_version: "13.0.0.1167"
---

# Managing Recovery Locations


Recovery locations consist of resource groups (that is, infrastructure objects such as vSphere hosts) used as target locations when orchestrating recovery. Resource groups are managed by the embedded Veeam ONE server installed on the Orchestrator server.

Orchestrator provides 4 types of recovery locations:

* VMware vSphere recovery locations that are used to define compute and storage resources in a VMware vSphere environment required when [running restore plans](running_restore.md) and [performing failback operations](running_failback.md).
* Microsoft Hyper-V recovery locations that are used to define cluster and storage resources in a Microsoft Hyper-V environment required when [running restore plans](running_restore.md).
* Storage recovery locations that are used to define target storage systems and compute resources required when [running storage plans](running_storage_failover.md).
* Microsoft Azure recovery locations that are used to define cloud resources required when [running cloud plans](running_cloud.md).


