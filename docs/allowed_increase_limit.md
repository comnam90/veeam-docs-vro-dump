---
title: "Allowed Increase Limit (All Licenses)"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/allowed_increase_limit.html"
last_updated: "12/10/2025"
product_version: "13.0.0.1167"
---

# Allowed Increase Limit (All Licenses)


Orchestrator allows you to increase the number of recovered VMs. The allowed license increase limit is defined by the license type.

Allowed Increase Limit (All Licenses)

| License Type | Allowed Increase Limit |
| Rental | 20 licenses or 20% of the license count (whichever is greater) |
| Subscription | 10 licenses or 10% of the license count (whichever is greater)  Note: 20 instances or 20% of the total instance count (whichever number is greater) if [automatic license update is enabled](updating_license_automatically.md) and you have successfully submitted the [license usage report](automatic_usage_reporting.md) within the last 30 days. |
| Perpetual | 10 licenses or 10% of the license count (whichever is greater)  Note: 20 instances or 20% of the total instance count (whichever number is greater) if [automatic license update is enabled](updating_license_automatically.md) and you have successfully submitted the [license usage report](automatic_usage_reporting.md) within the last 30 days. |

When the number of machines managed by Orchestrator exceeds the license limit, Orchestrator will treat them as follows:

* If the number of machines is within the allowed increase limit or less, Orchestrator will continue to manage all machines until your license expires.

To detect what machines will be managed, a FIFO (first-in first-out) queue is maintained: machines that were added to Orchestrator plans first will be included in the allowed exceed scope first. The license status of machines within the increase limit will be set to Licensed by exceed.

You must update the existing license by the license expiration date. Otherwise, the license status of machines within the increase limit will be set to Unlicensed, and these machines will no longer be managed by Orchestrator.

* If the number of machines is above the allowed exceed limit, the machines exceeding the licensed number plus the allowed increase limit will be excluded from management.

The license status of machines above the increase limit will be set to Unlicensed.


