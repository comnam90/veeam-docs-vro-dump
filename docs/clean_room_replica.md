---
title: "How Orchestrator Performs Failover in Clean Room"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/clean_room_replica.html"
last_updated: "2/11/2025"
product_version: "13.0.0.1167"
---

# How Orchestrator Performs Failover in Clean Room


In the [clean room scenario](infrastructure_clean_room.md), Orchestrator uses the following algorithm if you perform replica failover while the production Veeam Backup & Replication server is unavailable:

1. Orchestrator switches the failover process to the embedded Veeam Backup & Replication server.
2. Orchestrator rescans the VM replica to add information about this replica to the configuration database of the embedded Veeam Backup & Replication server.
3. Orchestrator completes the failover process.


