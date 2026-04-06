---
title: "Replica Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/replica_plans_overview.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Replica Plans


If you want to recover vSphere VMs protected by Veeam replication jobs, you can create a replica plan.

After you create and configure a replica plan, run a successful [readiness check](running_readiness_check.md), [malware scan](scanning_recovery_plans.md) and a [DataLab test](testing_recovery_plans.md), the plan can be considered ready for failover. You can invoke various actions for the plan, depending on the current plan state:

Replica Plans

| Point in Time | Actions |
| New plan created | After plan creation, you can:   * [Schedule a time for the plan to execute failover](scheduling_failover.md).  * [Run the plan to execute failover immediately](running_failover.md). |
| Failover | After failover, you can:   * [Perform permanent failover](running_permanent_failover.md).  * [Fail back to the original or to a new location](running_failback.md). |
| Failback | After failback, you can:   * [Commit failback](committing_failback.md). |
| Any | At any point, you can:   * [Halt the plan to interrupt its execution](halting_failover.md). * [Undo to attempt reversal of the previous action](undoing_halted_replica_plans.md). * [Reset the plan to clear the current state and allow it to run again](resetting_halted_replica_plans.md). |


