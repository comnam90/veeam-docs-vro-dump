---
title: "Roles"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/roles.html"
last_updated: "10/21/2025"
product_version: "13.0.0.1167"
---

# Roles


There are 3 roles that you can assign to users and user groups who will work with Orchestrator. Actions a user can perform depend on the role.

* Administrator — can perform all administration actions, and can also act as a Plan Author and Plan Operator.
* Plan Author — can enable, disable, reset, create, edit, test and scan plans.
* Plan Operator — can perform readiness checks, and can also test, scan, schedule and run plans that are enabled.

The following table describes the access available to users with different roles in the Orchestrator UI.

Roles

| Access | Administrator | Plan Author | Plan Operator |
| Administration | Full | None | None |
| Create, Edit, Enable, Disable, Reset, Delete Plans | Full | Full | Reset only |
| Check Plans | Full | Full | Full |
| Test Plans | Full | Full | Enabled plans only |
| Scan Plans | Full | Full | Enabled plans only |
| Schedule and Run Plans | Full | None | Enabled plans only |
| Reports and Templates | Full | Full | Read Only |


