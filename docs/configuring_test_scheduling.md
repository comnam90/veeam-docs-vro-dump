---
title: "Configuring Test Scheduling"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/configuring_test_scheduling.html"
last_updated: "10/31/2025"
product_version: "13.0.0.1167"
---

# Configuring Test Scheduling


To schedule recovery plan testing:

1. Navigate to DataLabs.
2. Choose the DataLab for which you want to create a schedule and click Schedule editor.
3. In the DataLab Schedule Editor window, click Add.
4. Complete the New Test Schedule wizard:

1. [Specify a schedule name and description](test_schedule_description.md).
2. [Specify scheduling settings](test_schedule_settings.md).
3. [Add lab groups and configure test options](test_schedule_groups.md).
4. [Select plans you want to test](test_schedule_plans.md).
5. [Choose whether you want to check restore points for possible malware](test_schedule_malware.md).
6. [Finish working with the wizard](test_schedule_finish.md).

|  |
| --- |
| Note |
| When Orchestrator tests a plan according to a specific schedule, the duration of the testing process equals the RTO value configured when creating the plan. If you instruct Orchestrator to test multiple plans at the same time, the duration of the testing process equals the maximum of the configured plan RTO values. Therefore, Orchestrator does not allow you to schedule other tests in the same DataLab until the RTO is over. |


