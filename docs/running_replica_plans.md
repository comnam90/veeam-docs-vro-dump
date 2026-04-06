---
title: "Running and Scheduling Replica Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/running_replica_plans.html"
last_updated: "12/26/2025"
product_version: "13.0.0.1167"
---

# Running and Scheduling Replica Plans


To run a replica plan, it must be ENABLED. To enable a plan:

1. Navigate to Recovery Plans.
2. Select the plan.
3. From the Manage menu, select Properties.

OR-

Right-click the plan name and select Manage > Properties.

1. Set the Availability toggle to Enabled.
2. Click Save.

If you do not enable a plan before you run it, the [Run Plan](running_failover.md) wizard will force you to do that as soon as you try running the plan.

|  |
| --- |
| Notes |
| 1. An Orchestrator Administrator or Plan Operator can force-enable a plan in the Run Plan wizard. However, a Plan Operator will not be able to run a disabled replica plan.   For more information on roles that can be assigned to users and user groups working with the Orchestrator UI, see [Managing User Accounts](managing_user_accounts.md).   1. For security purposes, all ‘real-world’ actions associated with replica plans (such as failover and failback) require password confirmation. |

In This Section

* [Scheduling Failover](scheduling_failover.md)
* [Running Failover](running_failover.md)
* [Halting Failover](halting_failover.md)
* [Finalizing Failover](finalizing_failover.md)
* [Undoing Failover](undoing_failover.md)
* [Undoing Failback](undoing_failback.md)
* [Resetting Replica Plans](resetting_replica_plans.md)
* [Halting Plan Testing](halting_replica_plan_testing.md)
* [Managing Halted Replica Plans](managing_halted_replica_plans.md)


