---
title: "Orchestrating Failback with NetApp Storage Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/failback_overview_netapp.html"
last_updated: "4/8/2024"
product_version: "13.0.0.1167"
---

# Orchestrating Failback with NetApp Storage Plans


After you run a NetApp storage plan and want to fail back to VMs running on source volumes, you must perform the following steps:

1. Add a new storage recovery location and specify the source volumes as target storage systems as described in section [Managing Recovery Locations](adding_storage_locations.md).
2. Reset the plan as described in section [Resetting Storage Plans](resetting_storage_plans.md).
3. Wait approximately 5 minutes for Orchestrator to collect data on the updated configuration.
4. Run a readiness check to ensure the plan is ready for failback as described in section [Running Plan Readiness Check](running_readiness_check.md).
5. Run the plan again as described in section [Running Storage Failover](running_storage_failover_netapp.md).

|  |
| --- |
| Tip |
| If the Reprotect storage volumes after failover check box at the Reprotect Volumes step of the [Run Plan wizard](running_storage_failover_netapp.md#reprotect) was not selected during the previous failover, you should first reverse the protection relationship between the source and destination volumes as described in the [NetApp ONTAP Documentation Center](https://docs.netapp.com/us-en/ontap-sm-classic/online-help-96-97/task_reverse_resynchronizing_snapmirror_relationships.html). |


