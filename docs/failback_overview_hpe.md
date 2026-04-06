---
title: "Orchestrating Failback with HPE Storage Plans"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/failback_overview_hpe.html"
last_updated: "6/20/2025"
product_version: "13.0.0.1167"
---

# Orchestrating Failback with HPE Storage Plans


After you run an HPE storage plan and want to fail back to VMs running on primary volumes, you must perform the following steps:

1. Add a new storage recovery location and specify the primary volumes as target storage systems as described in section [Managing Recovery Locations](adding_storage_locations.md).
2. Reset the plan as described in section [Resetting Storage Plans](resetting_storage_plans.md).
3. Wait approximately 5 minutes for Orchestrator to collect data on the updated configuration.
4. Run a readiness check to ensure the plan is ready for failback as described in section [Running Plan Readiness Check](running_readiness_check.md).
5. Run the plan again as described in section [Running Storage Failover](running_storage_failover_hpe.md).
6. Perform the start operation for the remote copy group as described in the [Hewlett Packard Enterprise Support Center](https://support.hpe.com/).

|  |
| --- |
| Tip |
| To trigger reverse replication and reprotect volumes included in the plan, do the following:   1. Perform the recover operation for the remote copy group as described in the [Hewlett Packard Enterprise Support Center](https://support.hpe.com/). 2. Connect to the target storage system through SSH and run the following command: setrcopygroup reverse -stopgroups -natural <remotecopygroupname> 3. Perform the start operation for the remote copy group as described in the [Hewlett Packard Enterprise Support Center](https://support.hpe.com/). |


