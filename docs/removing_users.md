---
title: "Removing User Accounts"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/removing_users.html"
last_updated: "1/20/2026"
product_version: "13.0.0.1167"
---

# Removing User Accounts


To remove a user account from Veeam Recovery Orchestrator, do the following:

1. Switch to the Administration page.
2. Navigate to Roles.
3. Remove each role assigned to the account. To do that, select the role and click Remove Account.

When you remove the last role assigned to the account, the account will be removed from the Orchestrator database automatically.

|  |
| --- |
| Note |
| There must always exist at least one user account with the Administrator role. This means that you cannot remove an Administrator account if you do not have any other Administrator accounts left. |

[![Removing User Account](images/removing_roles.webp)](images/removing_roles.webp "Removing User Account")


