---
title: "Cloud Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/cloud_plans_overview.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Cloud Plans


If you want to recover machines from vSphere VM and Veeam agent backups to a cloud environment, you can create a cloud plan.

After you create and configure a cloud plan, run a successful [readiness check](running_readiness_check.md) and [malware scan](scanning_recovery_plans.md), the plan can be considered ready for restore. You can invoke various actions for the plan, depending on the current plan state.

Cloud Plans

| Point in Time | Actions |
| New plan created | After plan creation, you can:   * [Schedule a time for the plan to execute restore](scheduling_cloud.md).  * [Run the plan to execute restore immediately](running_cloud.md). |
| Any | At any point, you can:   * [Halt the plan to interrupt its execution](halting_cloud.md).  * [Reset the plan to clear the current state and allow it to run again](resetting_cloud_plans.md). |


