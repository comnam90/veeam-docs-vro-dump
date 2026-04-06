---
title: "Restore Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/restore_plans_overview.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Restore Plans


If you want to recover vSphere VM, Hyper-V VM or Veeam agent backups to a VMware vSphere or Microsoft Hyper-V environment, create a restore plan.

After you create and configure a restore plan, run a successful [readiness check](running_readiness_check.md), [malware scan](scanning_recovery_plans.md) and a [DataLab test](testing_recovery_plans.md), the plan can be considered ready for restore. You can invoke various actions for the plan, depending on the current plan state.

Restore Plans

| Point in Time | Actions |
| New plan created | After plan creation, you can:   * [Schedule a time for the plan to execute restore](scheduling_restore.md).  * [Run the plan to execute restore immediately](running_restore.md). |
| Any | At any point, you can:   * [Halt the plan to interrupt its execution](halting_restore.md).  * [Reset the plan to clear the current state and allow it to run again](resetting_restore_plans.md). |


