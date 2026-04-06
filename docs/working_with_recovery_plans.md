---
title: "Working with Recovery Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/working_with_recovery_plans.html"
last_updated: "12/12/2025"
product_version: "13.0.0.1167"
---

# Working with Recovery Plans


Orchestrator offers 5 types of recovery plans:

* [Replica plans](working_with_replica_plans.md)
* [CDP replica plans](working_with_cdp_plans.md)
* [Restore plans](working_with_restore_plans.md)

* [Storage plans](working_with_storage_plans.md)
* [Cloud plans](working_with_cloud_plans.md)

Recovery plans are based on inventory groups. For more information on inventory groups, see [Inventory Groups](inventory_groups_overview.md).

|  |
| --- |
| Tip |
| To see the full list of discovered inventory groups, navigate to Scope Inventory. You can select any inventory group, click Add to Plan, and then click New Plan to create a recovery plan that will have the selected group preselected in the list of groups to recover. |

Recovery plans can be scheduled and chained to execute in sequence, and Orchestrator will automatically [produce and update detailed documentation](generating_reports.md). Execution of recovery plans is simplified to allow simultaneous management of multiple plans that contain hundreds of machines.


