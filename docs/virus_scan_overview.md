---
title: "How Orchestrator Performs Virus and YARA Scan"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/virus_scan_overview.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# How Orchestrator Performs Virus and YARA Scan


Performing On-Demand Virus and YARA Scan

When running on-demand scan for a restore or cloud plan, Orchestrator performs virus and YARA scan in the following way:

1. Disks of the machine that is being scanned are mounted to the [mount server](https://helpcenter.veeam.com/docs/backup/vsphere/mount_server.html?ver=120).
2. On the mount server, antivirus software and the configured YARA rule are triggered to scan files from the mounted disks.
3. Orchestrator iterates through the number of restore points [specified while running on-demand scan](scanning_plans_ondemand.md) one by one to detect a restore point with no viruses and malware.
4. If a clean restore point is detected, Orchestrator successfully completes the scan.

By default, Orchestrator checks only the most recent restore point on each machine. If all of these restore points are infected, the plan will acquire the NOT VERIFIED state after the scan process completes. However, if you [selected the Full image scan check box](scanning_plans_ondemand.md), Orchestrator will continue scanning the VM even after an infected restore point has been detected.

|  |
| --- |
| Note |
| If restore points of all machines included in the plan are stored in one repository, Orchestrator will process the machines one by one. This process may take a while, affecting the plan RTO. |

The results of virus and YARA scan are included in the [Plan Execution](viewing_plan_execution_history.md) report.

Performing Virus and YARA Scan During Plan Execution

When running a cloud or restore plan, Orchestrator performs virus and YARA scan in the following way:

1. Disks of a machine that is being restored are mounted to the [mount server](https://helpcenter.veeam.com/docs/backup/vsphere/mount_server.html?ver=120).
2. On the mount server, antivirus software and the configured YARA rule are triggered to scan files from the mounted disks.
3. Orchestrator iterates through the number of restore points specified while running the [restore](running_restore.md#Ransomware_restore) or [cloud plan](running_cloud.md#ransomware) one by one to detect a restore point with no viruses and malware.
4. If a clean restore point is detected, Orchestrator successfully restores the machine to the selected recovery location. If no clean restore point is detected, Orchestrator does one of the following:

* For restore plans — Orchestrator halts the plan or restores the machine to the selected recovery location without connecting it to any network, depending on the [configured restore point settings](running_restore.md#Ransomware_restore).
* For cloud plans — Orchestrator either halts the plan or restores the machine to a quarantine network depending on the [configured restore point settings](running_cloud.md#ransomware).

|  |
| --- |
| Note |
| If restore points of all machines included in the plan are stored in one repository, Orchestrator will process the machines one by one. This process may take a while, affecting the plan RTO. |

The results of virus and YARA scan are included in the [Plan Execution](viewing_plan_execution_history.md) report.

Performing Virus and YARA Scan During DataLab Test

When testing a restore plan, Orchestrator performs virus and YARA scan in the following way:

1. Disks of a machine that is being tested are mounted to the [mount server](https://helpcenter.veeam.com/docs/backup/vsphere/mount_server.html?ver=120).
2. On the mount server, antivirus software and the configured YARA rule are triggered to scan files from the mounted disks.
3. Orchestrator checks the most recent restore point for possible viruses and malware.
4. If the restore point is clean, the DataLab test completes successfully and Orchestrator restores the machine to the recovery location [selected when running the on-demand testing](starting_ondemand_test.md#labgroup).

If the restore point is infected, the DataLab test fails and the plan acquires the TESTING HALTED state. To learn how to manage halted testing, see [Halting Plan Testing](halting_restore_plan_testing.md).

The results of virus and YARA scan are included in the [DataLab Test](viewing_test_execution_history.md) report.


