---
title: "Managing YARA Rules"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/managing_yara_rules.html"
last_updated: "4/1/2025"
product_version: "13.0.0.1167"
---

# Managing YARA Rules


YARA is a tool that allows you to create malware detection patterns (rules) that can be customized to detect attacks and security threats specific to your environment. To perform YARA scan for a plan, you must import a YARA rule file to Orchestrator and then add this rule to the list of inventory items for a scope. When you run a plan with YARA scan enabled, Veeam Backup & Replication first mounts machine disks from backups to the mount server and then initiates a scan session.

You can use YARA scan to do the following:

* To find the most recent clean restore point. In this case the backup server iterates through the number of restore points specified while running the plan one by one to detect a restore point with no malware. If no clean restore point is found, the scan session completes with an error.

* To analyze the content of restore points for specific information (for example, sensitive data). If sensitive data is found, the scan session completes with an error.

If the scan session completes with an error, Orchestrator performs either of the following actions:

* When running a cloud plan, Orchestrator halts the plan or restores the machine to a quarantine network depending on the [configured restore point settings](running_cloud.md#ransomware).
* When running a restore plan, Orchestrator either halts the plan or restores the machine to the selected recovery location without connecting it to any network, depending on the [configured restore point settings](running_restore.md#ransomware_restore).

In This Section

[Adding YARA Rule Files](adding_yara.md)


