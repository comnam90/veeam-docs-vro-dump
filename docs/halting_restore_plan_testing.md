---
title: "Halting Plan Testing"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/halting_restore_plan_testing.html"
last_updated: "1/20/2026"
product_version: "13.0.0.1167"
---

# Halting Plan Testing


The Halt action interrupts plan testing. You may need to halt plan testing, for example, if you need to fix some environment-related issues and then [proceed with testing later](resuming_restore_plan_testing.md) (in this case, recovered VMs will still continue to run). Or you may need to stop the testing process completely, for example, if you no longer need to test the selected restore plan (in this case, recovered VMs will be deleted).

To halt testing of a restore plan:

1. Navigate to Recovery Plans.
2. Click the plan name to switch to the Plan Details page.
3. On the Plan Details page, select the plan and click Halt.
4. In the Halt Plan Test window, click Halt Plan Test to confirm the action.

[![Halting Plan Testing](images/halt_testing.webp)](images/halt_testing.webp "Halting Plan Testing")

To cancel testing of a restore plan:

1. Navigate to Recovery Plans.
2. Click the plan name to switch to the Plan Details page.
3. On the Plan Details page, select the plan and click Power Off.
4. In the Power Off Plan Testing window, click Power Off to confirm the action.

[![Halting Plan Testing](images/shutdown_testing.webp)](images/shutdown_testing.webp "Halting Plan Testing")


