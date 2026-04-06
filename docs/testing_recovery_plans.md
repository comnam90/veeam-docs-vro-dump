---
title: "Testing Recovery Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/testing_recovery_plans.html"
last_updated: "11/27/2025"
product_version: "13.0.0.1167"
---

# Testing Recovery Plans


Before you run a recovery plan, you can use an isolated Orchestrator DataLab to test the entire plan, including the verification of vSphere and agent backups, replicas and storage snapshots. All changes made to machines during a lab session will be discarded as soon as the testing process is over.

|  |
| --- |
| Note |
| DataLab testing is currently not supported for Microsoft Azure and Microsoft Hyper-V recovery locations. |

To test a recovery plan in a DataLab, perform a number of steps:

1. Create a virtual lab in Veeam Backup & Replication and [configure a connection to this lab](connecting_datalabs.md).
2. [Assign the DataLab to a scope](managing_inventory_items.md).
3. [Associate the DataLab with a recovery location](associating_datalabs.md).
4. [Optional] [Create a lab group](creating_lab_groups.md).
5. [Start on-demand testing](starting_ondemand_test.md) or [configure test scheduling settings](configuring_test_scheduling.md).


