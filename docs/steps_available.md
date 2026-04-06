---
title: "Steps Available"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/steps_available.html"
last_updated: "1/8/2026"
product_version: "13.0.0.1167"
---

# Steps Available


During failover to the DR site and restore to a recovery location, the Orchestrator server performs the list of steps described in this section.

Steps Available

| Plan Step | Restore Plan | | Replica Plan | CDP Replica Plan | Storage Plan | Cloud Plan |
| To VMware | To Hyper-V |
| [Check VM Heartbeat](check_vm_heartbeat.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Restore to Azure](create_cloud_vm.md) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) |
| [Generate Event](generate_event.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) |
| [Check Networks](ping_vm_network.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Prepare VM as Domain Controller](prepare_dc_for_lab.md)\* | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Process Replica VM (CDP)](process_cdp_replica_vm.md) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) |
| [Process Replica VM](process_replica_vm.md) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) |
| [Register Replica VM (Storage)](register_vm.md) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Restore VM](restore_vm.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) |
| [Send Email](send_email.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/Partially available.png) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) |
| [Shutdown Source VM](shutdown_source_vm.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/Partially available.png) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) |
| [Start Service](start_service.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/Partially available.png) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Veeam Job Actions](veeam_job_actions.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) |
| [Verify DNS Port](verify_dns_port.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Domain Controller Port](verify_dc_port.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Exchange Mailbox](verify_exchange_mailbox.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Exchange MAPI Connectivity](verify_mapi_connectivity.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Exchange Services](verify_exchange_mailbox.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Global Catalog Port](verify_gc_port.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Mail Server Port](verify_mail_server_port.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify SharePoint URL](verify_sharepoint_url.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify SQL Database](verify_sql_database.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify SQL Port](verify_sql_port.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Web Server Port](verify_web_server_port.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [Verify Web Site (IIS)](verify_iis.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) |
| [VM Power Actions](vm_power_actions.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) |
| [Custom Script](custom_script.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/yes.webp) |
| [Protect VM Group](protect_vm_group.md) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/yes.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) | ![Steps Available](images/no.webp) |

\*This step is available for DataLab testing only.


