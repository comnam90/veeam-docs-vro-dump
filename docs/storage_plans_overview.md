---
title: "Storage Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/storage_plans_overview.html"
last_updated: "5/9/2025"
product_version: "13.0.0.1167"
---

# Storage Plans


If you want to recover volumes protected by storage replication, you can create a storage plan.

After you create and configure a storage plan, run a successful [readiness check](running_readiness_check.md) and a [DataLab test](testing_recovery_plans.md), the plan can be considered ready for failover. You can invoke various actions for the plan, depending on the current plan state.

Storage Plans

| Point in Time | Actions |
| New plan created | After plan creation, you can:   * [Schedule a time for the plan to execute failover](scheduling_storage_failover.md).  * [Run the plan to execute failover immediately](running_storage_failover.md). |
| Any | At any point, you can:   * [Halt the plan to interrupt its execution](halting_storage_failover.md). * [Undo to attempt reversal of the previous action](undoing_halted_storage_plans.md).  * [Reset the plan to clear the current state and allow it to run again](resetting_storage_plans.md) (for example, to fail back). |

|  |
| --- |
| Important |
| After the storage failover process completes, Orchestrator will leave the plan in the IN-USE mode. By design, this makes the results of the storage failover process accessible in the Orchestrator UI as long as required, and also prevents the plan from being modified by any automatic updates related to infrastructure changes. Reset the plan if you want to perform any further actions with the plan (for example, to test the plan, to run readiness checks or to execute the plan again). |


