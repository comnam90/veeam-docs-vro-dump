---
title: "How Orchestrator Selects Backup Files"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/understanding_backup_file_selection.html"
last_updated: "1/2/2026"
product_version: "13.0.0.1167"
---

# How Orchestrator Selects Backup Files


Generally, when performing restore to a recovery location, Orchestrator looks through the list of all restore points created for a machine to choose a restore point that meets the date requirement specified in the [Run Plan wizard](running_restore.md#restorepoint). The backup file that contains the chosen restore point is used to recover the machine.

However, when you use [backup copy capabilities offered by Veeam Backup & Replication](https://helpcenter.veeam.com/docs/backup/vsphere/backup_copy.html?ver=120), you have multiple instances of the same backup data existing in different locations. This situation may influence the way Orchestrator chooses backup files to recover machines.

When you create or edit a [VMware recovery location](restore_location_recovery_options.md), you can choose either of the following recovery options:

* Automatic — the solution will use the backup file produced by either a primary or backup copy job. In case there are multiple primary and backup copy jobs, the solution will use the backup file that contains the most recent restore point regardless of whether this file is stored in a regular or scale-out backup repository.
* Primary — the solution will use the backup file produced by a primary backup job only. In case there are multiple primary and backup copy jobs, the solution will always use the backup file produced by the primary job that contains the most recent restore point regardless of whether this file is stored in a regular or scale-out backup repository.
* Backup Copy — the solution will use the backup file produced by a backup copy job. In case there are multiple primary and backup copy jobs, the solution will always use the backup file produced by the backup copy job that contains the most recent restore point regardless of whether this file is stored in a regular or scale-out backup repository.

Note that if you do not have any files produced by a backup copy job, the restore operation will complete with an error.

* SOBR Capacity Tier — the solution will use the backup file stored in a capacity tier of a scale-out backup repository only. The solution will always use the backup file produced by any backup job (either primary or backup copy) that contains the most recent restore point.

Note that if you do have any backup files with restore points stored in a scale-out backup repository, the restore operation will complete with an error.

|  |
| --- |
| Note |
| When you [move backup files of a backup copy job](https://helpcenter.veeam.com/docs/backup/vsphere/backup_moving.html?ver=120) to another repository in the Veeam Backup & Replication console, Orchestrator becomes unable to use the restore points of the moved backup files for restore because of incorrect timestamps. That is why make sure to run both the backup job and the backup copy job to create new restore points after you perform the move operation. |


