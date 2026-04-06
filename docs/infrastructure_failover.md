---
title: "Scenario 5: Orchestrating VM Replica Failover"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/infrastructure_failover.html"
last_updated: "4/1/2025"
product_version: "13.0.0.1167"
---

# Scenario 5: Orchestrating VM Replica Failover


This deployment scenario illustrates recovery based on vSphere VM replicas created by Veeam Backup & Replication.

In this scenario, you can switch from the original VMs in the production site to the VM replicas in the disaster recovery (DR) site. The Orchestrator server provides failover plan management, testing and execution, failing over all VMs and performing verification tests and checks to ensure successful recovery.

![Scenario 5: Orchestrating VM Replica Failover](images/failover_diagram.webp)


