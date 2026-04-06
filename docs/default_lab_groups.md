---
title: "Working with Default Lab Groups"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/default_lab_groups.html"
last_updated: "10/20/2025"
product_version: "13.0.0.1167"
---

# Working with Default Lab Groups


Default lab groups are lab groups created by an Administrator but available for plan testing by Plan Authors and Plan Operators for any scope.

To allow Plan Authors and Plan Operators to use a lab group as a default group when testing plans for their scope:

1. Assign a DataLab to the scope as described in section [Managing Inventory Items](managing_inventory_items.md).
2. Add the lab group to the DataLab as described in section [Creating Lab Groups](creating_lab_groups.md).

The added lab group will now be considered a default lab group. The DataLab with the lab group will become available for the scope, and Plan Authors and Plan Operators will be able to use the group for plan testing. The lab group will be preselected in the [Run Lab Tests](starting_ondemand_test.md) and [Create Test Schedule](configuring_test_scheduling.md) wizards, and it will start before all other lab groups in the DataLab every time Orchestrator powers on the lab to test a recovery plan.

|  |
| --- |
| Note |
| Plan Authors and Plan Operators cannot edit default lab groups or delete them from DataLabs because these groups can be managed only by Administrators. However, if an Administrator assigns a DataLab to the Default Scope, lab groups added to the DataLab will not be treated as default lab groups. This means that Plan Authors will still be able to edit and delete these lab groups as described in section [Configuring Lab Groups](configuring_lab_groups.md). |


