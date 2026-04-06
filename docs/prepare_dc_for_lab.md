---
title: "Prepare VM as Domain Controller"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/prepare_dc_for_lab.html"
last_updated: "1/8/2026"
product_version: "13.0.0.1167"
---

# Prepare VM as Domain Controller


This step prepares a domain controller running on the selected VM to perform an authoritative restore. This will always be the first step to execute for the VM.

For more information on performing an authoritative restore of a domain controller, see [Microsoft Docs](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/forest-recovery-guide/ad-forest-recovery-authoritative-recovery-sysvol) and [this Veeam KB article](https://www.veeam.com/blog/how-to-recover-a-domain-controller-best-practices-for-ad-protection.html).

|  |
| --- |
| Important |
| Before you restore a domain controller, you must enable application-aware processing for the selected VM in Veeam Backup & Replication as described in the Veeam Backup & Replication User Guide, section [Enable Application-Aware Processing](https://helpcenter.veeam.com/docs/vbr/userguide/backup_job_vss_application_vm.html?ver=13). |

The Prepare VM as Domain Controller step has the following parameters, but they are not editable:

Prepare VM as Domain Controller

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for VM recovery.  If you mark the step as Critical, its failure for a VM from a critical inventory group will halt the plan. | Yes |


