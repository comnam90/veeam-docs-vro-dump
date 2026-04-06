---
title: "Managing Scopes"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/managing_scopes.html"
last_updated: "1/20/2026"
product_version: "13.0.0.1167"
---

# Managing Scopes


Orchestrator controls access to its functionality with the help of scopes. A scope defines the access that users have to inventory items such as inventory groups, plan steps, recovery locations, template jobs, credentials, DataLabs and YARA rules. These inventory items are used to build recovery plans.

For a scope, you can:

1. [Assign roles to users in a scope](managing_user_accounts.md).

After you install Orchestrator, you will have one scope only — the Default Scope. By design, all items discovered by the solution are added to this scope, including items collected from connected Veeam Backup & Replication servers (such as inventory groups, credentials, template jobs and so on).

You can remove items from the Default Scope; however, it is recommended that you create additional scopes to provide more granular permissions to users for enhanced security — to do that, follow the instructions provided in section [Creating Scopes](creating_scopes.md).

1. Limit the number of inventory items available in the Orchestrator UI to users from that scope.

All newly-created scopes will NOT automatically have any visibility of newly discovered inventory items until those items are explicitly added to that scope. To add an item to a scope, navigate to Scope Inventory and follow the instructions provided in sections [Managing Inventory Items](managing_inventory_items.md) and [Connecting DataLabs](connecting_datalabs.md).


