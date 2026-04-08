---
title: "Scheduling Restore"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/scheduling_restore.html"
last_updated: "4/8/2026"
product_version: "13.0.0.1167"
---

# Scheduling Restore


You can schedule a time for a restore plan to execute. To do that:

1. Navigate to Recovery Plans.
2. Select the plan. From the Launch menu, select Manage > Schedule.

-OR-

Right-click the plan name and select Manage > Schedule.

1. In the Scheduled Tasks window, do the following:

1. Set the Schedule plan execution toggle to Enabled.
2. Click the Configure schedule link and choose whether you want to run the plan on schedule or after any other plan:

* If you want to run the plan at a specific time, click the Schedule icon in the Run on field, set the desired date and time, and click Apply.
* If you want to run the plan after another plan, select the Schedule after plan check box and click Choose plan. Then, in the Select Plan window, select the necessary plan and click Apply.

For a plan to be displayed in the list of available plans, it must be ENABLED as described in section [Running and Scheduling Restore Plans](running_restore_plans.md#enablingplans).

1. Set the Malware actions toggle to Enabled if you want to check restore points created for machines included in the plan for malware flags. When restoring to a VMware vSphere environment, you can also decide whether you want to scan these restore points with antivirus software, YARA rules or both.

By default, Orchestrator checks the most recent restore point on each machine. If all the restore points are infected, Orchestrator restores the machine to the selected recovery location without connecting it to any network. However, you can instruct Orchestrator to halt the plan and cancel the restore operation if no clean restore point is found.

For more information on how Orchestrator performs malware scan, see [Overview](malware_scan_overview.md).

1. Review the configuration information and click Save.

|  |
| --- |
| Tip |
| You can also scan a recovery plan for possible malware without scheduling the plan execution. To do that, follow the instructions provided in section [Scanning Recovery Plans](scanning_recovery_plans.md). |

[![Scheduling Restore](images/restore_plan_schedule.webp)](images/restore_plan_schedule.webp "Scheduling Restore")

|  |
| --- |
| Tip |
| You can disable a configured schedule if you no longer need it. To do that, set the Schedule plan execution toggle to Disabled in the Scheduled Tasks window. |


