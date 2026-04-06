---
title: "Step 16. Upgrade to Veeam Backup & Replication 13"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/install_vbr.html"
last_updated: "1/2/2026"
product_version: "13.0.0.1167"
---

# Step 16. Upgrade to Veeam Backup & Replication 13


It is essential that you upgrade to version 13 every remote Veeam Backup & Replication server that is connected to Orchestrator. Otherwise, the new functionality in Orchestrator version 13 will not be available. To upgrade Veeam Backup & Replication to version 13, follow the instructions provided in the Veeam Backup & Replication User Guide, section [Upgrade and Update](https://helpcenter.veeam.com/docs/vbr/userguide/vbr_updating.html?ver=13), and in [this Veeam KB article](https://www.veeam.com/kb4738).

After the upgrade process completes, open the Veeam Backup & Replication console on the Orchestrator server to update Veeam Backup & Replication components installed on all managed servers. To perform the update, follow the steps of the Components Update wizard. For more information on updating server components, see the Veeam Backup & Replication User Guide, section [Updating Infrastructure Components](https://helpcenter.veeam.com/docs/vbr/userguide/components_update.html?ver=13).

|  |
| --- |
| Tip |
| If you want to use the embedded Veeam Backup & Replication server to run backup and replication jobs along with orchestration, create jobs on that server. Orchestrator will discover backups and replicas produced by these jobs and will use them for recovery plans. To learn how to create jobs using Veeam Backup & Replication, see the Veeam Backup & Replication User Guide, sections [Creating Backup Jobs](https://helpcenter.veeam.com/docs/vbr/userguide/backup_job.html?ver=13) and [Creating Replication Jobs](https://helpcenter.veeam.com/docs/vbr/userguide/replica_job.html?ver=13). |


