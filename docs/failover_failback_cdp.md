---
title: "Failover and Failback"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/failover_failback_cdp.html"
last_updated: "11/24/2025"
product_version: "13.0.0.1167"
---

# Failover and Failback


Failover is a process of switching from the original VM in the production site to its VM replica in the recovery site. Orchestrator provides you with a number of options to finalize failover to VM replicas:

* Permanent Failover — as a result, VM replicas in the disaster recovery site will no longer be treated as replicas. Restore point snapshots will be deleted, and the source VMs will be removed from CDP policies.

For more information on the permanent failover process, see the Veeam Backup & Replication User Guide, section [Permanent Failover](https://helpcenter.veeam.com/docs/vbr/userguide/cdp_permanent_failover.html?ver=13).

* Failback — you can choose whether you want to fail back to the original or to a new location.

* If failing back to the original location, you will switch from VM replicas back to the source VMs. The source VMs will be restored to the current state of their replicas.
* If failing back to a new location, all VM replica files will be transported to the location and used to recover the VMs there.

Failback is a temporary stage that must be further finalized. After confirming that the failed-back VMs operate correctly, you can perform the Commit failback operation. Alternatively, [undo failback](undoing_failback_cdp.md) to return the plan back to the FAILOVER state.

For more information on the replica failback process, see the Veeam Backup & Replication User Guide, sections [Failback](https://helpcenter.veeam.com/docs/vbr/userguide/cdp_failback.html?ver=13) and [Commit Failback](https://helpcenter.veeam.com/docs/vbr/userguide/cdp_failback_commit.html?ver=13).

Depending on the selected option, the plan may enter the PERMANENT FAILOVER, FAILBACK, COMMIT FAILBACK or HALTED state. To learn how to work with HALTED CDP replica plans, see [Managing Halted Plans](managing_halted_cdp_plans.md).


