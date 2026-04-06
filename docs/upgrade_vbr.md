---
title: "Step 13. Upgrade to Veeam Backup & Replication 13"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/upgrade_vbr.html"
last_updated: "1/20/2026"
product_version: "13.0.0.1167"
---

# Step 13. Upgrade to Veeam Backup & Replication 13


It is essential that you upgrade to version 13 every remote Veeam Backup & Replication server connected to Orchestrator — this version contains numerous enhancements and fixes required for the Orchestrator integration. To upgrade Veeam Backup & Replication to version 13, follow the instructions provided in the Veeam Backup & Replication User Guide, section [Upgrading to Veeam Backup & Replication 13](https://helpcenter.veeam.com/docs/vbr/userguide/vbr_updating.html?ver=13), and in [this Veeam KB article](https://www.veeam.com/kb4738).

After the upgrade process completes, do the following:

1. Open the Veeam Backup & Replication console on each remote Veeam Backup & Replication server to update configured virtual labs. To perform the update, follow the steps of the Edit Virtual Lab wizard.

For more information on editing Veeam Backup & Replication virtual labs, see the Veeam Backup & Replication User Guide, section [Editing and Deleting Virtual Labs](https://helpcenter.veeam.com/docs/vbr/userguide/vlab_edit_delete.html?ver=13).

1. Open the Veeam Backup & Replication console on each remote Veeam Backup & Replication server to update Veeam Backup & Replication components installed on all managed servers. To perform the update, follow the steps of the Components Update wizard.

For more information on updating server components, see the Veeam Backup & Replication User Guide, section [Updating Infrastructure Components](https://helpcenter.veeam.com/docs/vbr/userguide/components_update.html?ver=13).

1. Open the Orchestrator UI and make sure all Orchestrator agents running on remote Veeam Backup & Replication servers have also been upgraded successfully.

To do that, switch to the Administration page, navigate to Infrastructure and check the status of each connected Veeam Backup & Replication server. If you encounter a connection issue with an Orchestrator agent, repair the agent as described in section [Repairing Orchestrator Agents](repairing_vro_agents.md).


