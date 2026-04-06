---
title: "License Expiration"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/license_expiration.html"
last_updated: "1/3/2024"
product_version: "13.0.0.1167"
---

# License Expiration


Orchestrator license period is set in accordance with the chosen licensing program. When this period is over, you must update the license.

To ensure a smooth license update and provide sufficient time to install a new license file, Orchestrator offers a grace period after the license expiration date. During the grace period, Orchestrator keeps working in a full-version mode. The license status during this period appears as Your license has expired and needs to be renewed.

The duration of the grace period is defined by the license type:

License Expiration

| License Type | Expiration Grace Period |
| Perpetual | Not applicable |
| Rental | 60 days |
| Subscription | 30 days |

You must update the license before the end of the grace period. If you do not update the license, Orchestrator will stop executing recovery plans as soon as the grace period ends. Plan testing will be disabled as well.

To learn how to update Orchestrator license, see [Updating License](updating_license.md).

Recovered VM License Statuses

In Orchestrator, a recovered VM can have one of the following license statuses:

* Licensed — the machine has licenses assigned and is fully managed by Orchestrator.
* [Applies only to Rental licenses] New — the machine was added to a recovery plan within the current calendar month. The machine will be fully managed by Orchestrator until the end of the current month.
* Unlicensed — the machine does not have licenses assigned, as there are no more licenses in the license pool. The unlicensed machine will have either the Licensed by Exceed or Unlicensed status.

* Licensed by Exceed — the machine has no licenses assigned but is within the allowed increase limit. The machine can be used in recovery plans until the end of the grace period.
* Unlicensed by Exceed — the machine has no licenses assigned, and the allowed increase limit was exceeded. The machine will not be managed by Orchestrator.

For more information, see [Exceeding License Limit](exceeding_license_limit.md).


