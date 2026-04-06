---
title: "Running and Scheduling Restore Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/running_restore_plans.html"
last_updated: "12/26/2025"
product_version: "13.0.0.1167"
---

# Running and Scheduling Restore Plans


|  |
| --- |
| Important |
| When restoring a VM to a Hyper-V environment while the source VM still exists in the original location, Orchestrator may create a new VM using the same MAC address as the source VM. To avoid network issues and MAC address conflicts, it is recommended that you power the source VM off before you run the restore plan. |

To run a restore plan, it must be ENABLED. To enable a plan:

1. Navigate to Recovery Plans.
2. Select the plan.
3. From the Manage menu, select Properties.

OR-

Right-click the plan name and select Manage > Properties.

1. Set the Availability toggle to Enabled.
2. Click Save.

If you do not enable a plan before you run it, the [Run Plan](running_restore.md) wizard will force you to do that as soon as you try running the plan.

|  |
| --- |
| Notes |
| 1. An Orchestrator Administrator or Plan Operator can force-enable a plan in the Run Plan wizard. However, a Plan Operator will not be able to run a disabled restore plan.   For more information on roles that can be assigned to users and user groups working with the Orchestrator UI, see [Managing User Accounts](managing_user_accounts.md).   1. For security purposes, all ‘real-world’ actions associated with restore plans require password confirmation. |

In This Section

* [Scheduling Restore](scheduling_restore.md)
* [Running Restore](running_restore.md)
* [Halting Restore](halting_restore.md)
* [Resetting Restore Plans](resetting_restore_plans.md)
* [Halting Plan Testing](halting_restore_plan_testing.md)
* [Managing Halted Restore Plans](managing_halted_restore_plans.md)


