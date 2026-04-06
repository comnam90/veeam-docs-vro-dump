---
title: "Upgrading Veeam Recovery Orchestrator"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/upgrading_vro.html"
last_updated: "1/20/2026"
product_version: "13.0.0.1167"
---

# Upgrading Veeam Recovery Orchestrator


Upgrade to Orchestrator version 13 is supported from Orchestrator version 7.2.1 only; upgrade from Orchestrator versions 7.2, 7.1, 7, 6 and 5 to version 13 is not supported:

* To learn how to manually upgrade from Orchestrator version 7.2 to 7.2.1, see [Veeam Recovery Orchestrator 7.2 User Guide](https://helpcenter.veeam.com/docs/vro/userguide/upgrading_vro.html?ver=7.2).
* To learn how to manually upgrade from Orchestrator version 7.1 to 7.2, see [Veeam Recovery Orchestrator 7.2 User Guide](https://helpcenter.veeam.com/docs/vro/userguide/upgrading_vro.html?ver=7.2).
* To learn how to manually upgrade from Orchestrator version 7 to 7.1 and from Orchestrator version 6 to 7, see [Veeam Recovery Orchestrator 7 User Guide](https://helpcenter.veeam.com/docs/vro/userguide/upgrading_vro.html?ver=70).
* To learn how to manually upgrade from Orchestrator version 5 to 6, see the [Veeam Disaster Recovery Orchestrator 6 User Guide](https://helpcenter.veeam.com/docs/vdro/userguide/upgrading_vdro.html?ver=60).

Upgrade Checklist

Check the following prerequisites before upgrading Orchestrator:

1. Perform backup of all existing databases that are used to store data collected from Orchestrator, Veeam Backup & Replication and Veeam ONE, and create a snapshot of the Orchestrator server — so that you can easily go back to the previous version in case of upgrade issues.
2. Make sure there is enough space for upgrade of the Microsoft SQL Server configuration database. To calculate the required space, add at least 25% of free space to the size of the Microsoft SQL Server configuration database.

By default, the setup wizard installs Orchestrator with Microsoft SQL Server Express. Note that the maximum configuration database size for Microsoft SQL Server Express is 10 GB.

1. Make sure there are no recovery plans being tested or executed (that is, no plans are in the IN-USE mode, HALTED state or any of the active states).

For the list of modes and states that different types of recovery plans can acquire, see [Replica Plans](states_modes_replica.md), [CDP Replica Plans](states_modes_cdp.md), [Restore Plans](states_modes_restore.md), [Storage Plans](states_modes_storage.md) and [Cloud Plans](states_modes_cloud.md).

1. Make sure there are no recovery plans scheduled to run during upgrade. Otherwise, disable the configured schedule as described in sections [Scheduling Failover](scheduling_failover.md), [Scheduling CDP Failover](scheduling_failover_cdp.md), [Scheduling Restore](scheduling_restore.md), [Scheduling Storage Failover](scheduling_storage_failover.md) and [Scheduling Cloud Restore](scheduling_cloud.md).
2. Make sure all active Orchestrator UI sessions are closed.

Performing Upgrade

To upgrade to Orchestrator version 13, perform the following steps:

1. Make sure the machine where Orchestrator will be installed meets the prerequisite conditions described in section [System Requirements](system_requirements.md).
2. Download the latest version of the product installation image from the [Veeam downloads page](https://www.veeam.com/downloads.html). You can burn the downloaded image file to a CD/DVD or mount the installation image to the target machine using disk image emulation software.
3. [Launch the splash window](launch_splash_window_upgrade.md).
4. [Start the setup wizard](start_setup_upgrade.md).
5. [Accept the license agreement](accept_license_agreement_upgrade.md).
6. [Review components to upgrade](review_components_upgrade.md).
7. [Provide a license file](provide_license_file_upgrade.md).
8. [Perform system configuration check](perform_configuration_check_upgrade.md).
9. [Specify service account credentials](specify_service_credentials_upgrade.md).
10. [Review SQL server connection settings](review_sql_server_upgrade.md).
11. [Choose a PostgreSQL server](choose_postgresql_server_upgrade.md).
12. [Review configuration issues](review_configuration_issues_upgrade.md).
13. [Specify the Veeam ONE caching port](specify_caching_port_upgrade.md).
14. [Review installation summary](review_upgrade_summary.md).
15. [Begin upgrade](review_upgrade_summary.md).
16. [Upgrade remote Veeam Backup & Replication servers to version 13](upgrade_vbr.md).

|  |
| --- |
| Important |
| The embedded Veeam Backup & Replication and Veeam ONE servers are upgraded automatically, as part of the Orchestrator server upgrade process. DO NOT try to upgrade the embedded servers manually, by using the installation images of remote Veeam Backup & Replication and Veeam ONE solutions. Otherwise, the correct operation of the Orchestrator server cannot be guaranteed. |


