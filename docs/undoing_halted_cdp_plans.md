---
title: "Undoing Halted CDP Replica Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/undoing_halted_cdp_plans.html"
last_updated: "12/26/2025"
product_version: "13.0.0.1167"
---

# Undoing Halted CDP Replica Plans


To perform an undo operation for a HALTED CDP replica plan:

1. Navigate to Recovery Plans.
2. Select the plan and click Undo.
3. In the Undo window, do the following:

1. For security purposes, retype your password and click Next.
2. Review configuration information and click Undo. The failover process will be started.

[![Undoing Halted Plan](images/undo_halt_failover.webp)](images/undo_halt_failover.webp "Undoing Halted Plan")

If a plan repeatedly enters the HALTED state due to misconfiguration or changes in the external environment, the only option left may be to [RESET](resetting_halted_cdp_plans.md) the plan.


