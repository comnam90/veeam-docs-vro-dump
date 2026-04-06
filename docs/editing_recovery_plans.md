---
title: "Editing Recovery Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/editing_recovery_plans.html"
last_updated: "10/6/2025"
product_version: "13.0.0.1167"
---

# Editing Recovery Plans


In addition to default recovery plan settings that you specify when creating a plan, you can also specify granular settings to customize the plan. The Orchestrator UI allows you to adjust the following:

* [Plan properties](configuring_plan_properties.md)
* [Group settings](configuring_groups.md)
* [Plan step settings](configuring_steps.md)
* [Step parameter settings](configuring_step_parameters.md)

|  |
| --- |
| Note |
| You cannot edit a recovery plan if the plan is in the IN-USE mode. If a recovery plan is in the ENABLED mode, you can edit only plan properties. To allow editing plan properties and other plan settings, you must disable the plan.  For the list of modes that different types of recovery plans can acquire, see [Replica Plans](states_modes_replica.md), [CDP Replica Plans](states_modes_cdp.md), [Restore Plans](states_modes_restore.md), [Storage Plans](states_modes_storage.md) and [Cloud Plans](states_modes_cloud.md). |


