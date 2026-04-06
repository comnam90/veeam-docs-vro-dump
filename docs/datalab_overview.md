---
title: "DataLabs"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/datalab_overview.html"
last_updated: "12/12/2025"
product_version: "13.0.0.1167"
---

# DataLabs


Orchestrator DataLabs are based on Veeam Backup & Replication virtual labs. While a Veeam Backup & Replication virtual lab is an appliance VM that creates an isolated network, Orchestrator adds the capability to easily create multiple test environments, to perform recovery and application verification including custom scripts, and to generate detailed reporting.

DataLabs may be powered on independently from recovery plans and used for other test cases (for example, to test patches or upgrades). You can add one or more recovery plans to any running lab and verify the plans there. You may choose to keep the lab running, so that additional tests can be performed.

To test a recovery plan:

1. In the Veeam Backup & Replication console, create a virtual lab that will be used to start vSphere and agent backups, replicas and storage snapshots.

For more information, see the Veeam Backup & Replication User Guide, section [Virtual Lab](https://helpcenter.veeam.com/docs/vbr/userguide/virtual_lab.html?ver=13).

|  |
| --- |
| Important |
| When creating a virtual lab, consider the following:   * To test a replica, CDP replica or restore plan, the virtual lab must be created on a Veeam Backup & Replication server that manages backup and replication jobs protecting machines included in the plan. * To test a storage plan, the virtual lab must be created on a Veeam Backup & Replication server that protects the storage system where VMs included in the plan belong. If the storage system is not protected by any Veeam Backup & Replication server, the virtual lab must be created on the embedded Veeam Backup & Replication server. |

1. Assign the lab to the required scope.

For more information, see [Connecting DataLabs](connecting_datalabs.md).

1. [Create a lab group to provide the test environment for the vSphere and agent backups, replicas and storage snapshots to be verified](creating_lab_groups.md).

Most VMs require a domain controller to boot and start services successfully. If the recovery plan does not include a domain controller, ensure that the lab group includes a VM with the Domain Controller role, and that this VM has a correct IP addressing scheme for the DR site. Otherwise, the VMs in the plan will fail to verify.

1. [Start on-demand plan testing](starting_ondemand_test.md) or [configure test scheduling](configuring_test_scheduling.md).

To ensure that a recovery plan is automatically and regularly verified, you can schedule the plan for automated lab testing.

|  |
| --- |
| Note |
| The test will not run unless the plan is in the ENABLED or DISABLED mode. The test will also not run if the plan is currently being edited.  For the list of modes that different types of recovery plans can acquire, see [Replica Plans](states_modes_replica.md), [CDP Replica Plans](states_modes_cdp.md), [Restore Plans](states_modes_restore.md) and [Storage Plans](states_modes_storage.md). |


