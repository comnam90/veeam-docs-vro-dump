---
title: "Scheduling Failover"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/scheduling_failover_cdp.html"
last_updated: "12/26/2025"
product_version: "13.0.0.1167"
---

# Scheduling Failover


You can schedule a time for a CDP replica plan to execute. Only the failover process can be scheduled — all other operations (failback, undo failover and so on) must be performed manually in the Orchestrator UI.

To schedule a CDP replica plan:

1. Navigate to Recovery Plans.
2. Select the plan. From the Manage menu, select Schedule.

-OR-

Right-click the plan name and select Manage > Schedule.

1. In the Scheduled Tasks window, do the following:

1. Set the Schedule plan execution toggle to Enabled.
2. Click the Configure schedule link and choose whether you want to run the plan on schedule or after any other plan:

* If you want to run the plan at a specific time, click the Schedule icon in the Run on field, set the desired date and time, and click Apply.
* If you want to run the plan after another plan, select the Schedule after plan check box and click Choose plan. Then, in the Select Plan window, select the necessary plan and click Apply.

For a plan to be displayed in the list, it must be ENABLED as described in section [Running and Scheduling Restore Plans](running_restore_plans.md#enablingplans).

1. Set the Malware actions toggle to Enabled if you want to check restore points created for machines included in the plan for malware flags.

For more information on how Orchestrator performs malware scan, see [Overview](malware_scan_overview.md).

1. Review the configuration information and click Save.

|  |
| --- |
| Tip |
| You can also scan a recovery plan for possible malware without scheduling the plan execution. To do that, follow the instructions provided in section [Scanning Recovery Plans](scanning_recovery_plans.md). |

[![Scheduling Failover](images/schedule_replica.webp)](images/schedule_replica.webp "Scheduling Failover")

|  |
| --- |
| Tip |
| You can disable a configured schedule if you no longer need it. To do that, set the Schedule plan execution toggle to Disabled in the Scheduled Tasks window. |


