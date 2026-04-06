---
title: "Configuring Veeam Recovery Orchestrator"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/configuring_vro.html"
last_updated: "6/27/2025"
product_version: "13.0.0.1167"
---

# Configuring Veeam Recovery Orchestrator


To start working with Orchestrator, perform a number of steps for its configuration:

1. Configure access to Orchestrator:

1. [Create scopes to allow access to Orchestrator](managing_scopes.md).
2. [For each scope, add users to specific roles.](managing_user_accounts.md)
3. [Configure MFA](enabling_mfa.md).

1. Connect infrastructure:

1. [Connect Veeam Backup & Replication servers](connecting_backup_servers.md).
2. [Connect vCenter Servers](connecting_vsphere_servers.md).
3. [Connect Microsoft Hyper-V servers](connecting_scvmm_servers.md).
4. [Connect NetApp and HPE storage](connecting_storage_systems.md).

1. Create recovery locations:

1. [Create a VMware vSphere recovery location](adding_restore_locations.md).
2. [Create a storage recovery location](adding_storage_locations.md).
3. [Create a Microsoft Azure recovery location](adding_cloud_locations.md).
4. [Create a Microsoft Hyper-V recovery location](adding_hyperv_locations.md).

1. [Manage credentials under which recovery plan steps will be launched](managing_credentials.md).
2. [Manage plan steps to be performed while running the recovery process](configuring_plan_steps.md).
3. [Manage template jobs to be used to reprotect inventory groups in recovery plans](editing_template_jobs.md).
4. [Manage DataLabs to be used to test recovery plans](connecting_datalabs.md).
5. [Manage access to inventory items to be used in recovery plans](managing_inventory_items.md).
6. Configure general settings:

1. [Specify email server settings](specify_smtp_settings.md).
2. [Specify report subscription settings](specify_email_settings.md).
3. [Configure report retention settings](configuring_report_options.md).


