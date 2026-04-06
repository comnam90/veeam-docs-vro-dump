---
title: "Permissions"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/permissions.html"
last_updated: "1/22/2026"
product_version: "13.0.0.1167"
---

# Permissions


The accounts used to install and administer Orchestrator must have the following permissions.

Permissions

| Account | Required Permission |
| Setup Account | The account used for product installation must be a domain or local account that has the local Administrator permissions on the target machine. |
| Orchestrator Service Accounts | The accounts used to run Orchestrator services, Veeam Backup & Replication services and Veeam ONE services must have the local Administrator permissions on the Orchestrator server.  The accounts must also be granted the Log on as a service right. For more information on Windows security policy settings, see [Microsoft Docs](https://docs.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/log-on-as-a-service). |
| Orchestrator Agent Account | The account used to install and run the Orchestrator agent on a Veeam Backup & Replication server must have the local Administrator, the Veeam Backup Administrator and the database Administrator permissions on the server. |
| Orchestrator User Accounts | The accounts used to log in to the Orchestrator UI must be granted the Allow log on locally right. For more information on Windows security policy settings, see [Microsoft Docs](https://docs.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/allow-log-on-locally). |
| vCenter Server Permissions | The account used to connect the vCenter Server to Orchestrator must have administrative permissions. You can either grant the Administrator role to the account or configure more granular permissions. For more information, see [Veeam Backup & Replication Required Permissions](https://helpcenter.veeam.com/docs/vbr/userguide/required_permissions.html?ver=13#using-virtualization-servers-and-hosts) and [Veeam ONE Required Permissions](https://helpcenter.veeam.com/docs/one/userguide/connection_to_virtual_servers.html?ver=13).  To be able to open sessions on the vCenter Server system, the account must also have the Sessions.Validate session privilege on the root vCenter Server. For more information on session privileges, see [VMware Docs](https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/vsphere/8-0/vsphere-security-8-0/defined-privileges/sessions-privileges.html). |
| SCVMM Server Permissions | The account used to connect the SCVMM server to Orchestrator must have administrative permissions. You can either grant the Administrator role to the account or configure more granular permissions. For more information, see [Veeam Backup & Replication Required Permissions](https://helpcenter.veeam.com/docs/vbr/userguide/required_permissions.html?ver=13#using-virtualization-servers-and-hosts) and [Veeam ONE Required Permissions](https://helpcenter.veeam.com/docs/one/userguide/connection_to_virtual_servers.html?ver=13#microsoft-scvmm). |
| Microsoft Hyper-V and Azure Local Cluster Permissions | The account used to connect the standalone Microsoft Hyper-V or Azure Local cluster to Orchestrator must have administrative permissions. You can either grant the Administrator role to the account or configure more granular permissions. For more information, see [Veeam Backup & Replication Required Permissions](https://helpcenter.veeam.com/docs/vbr/userguide/required_permissions.html?ver=13#using-virtualization-servers-and-hosts) and [Veeam ONE Required Permissions](https://helpcenter.veeam.com/docs/one/userguide/connection_to_virtual_servers.html?ver=13#microsoft-hyper-v-hosts-and-clusters). |
| Microsoft SQL Server Permissions | Different sets of Microsoft SQL permissions are required in the following cases:   * Installation (remote or local): the current account needs the CREATE ANY DATABASE permission on the SQL server level. After the database is created, this account automatically gets a db\_owner role and can perform all operations with the database. * Operation: the account used to run Orchestrator, Veeam Backup & Replication and Veeam ONE services requires the following permissions:  * The db\_owner permission and permissions to execute stored procedures for the configuration databases on the Microsoft SQL Server. * The db\_datareader permissions to read data from the SQL server master database. * The public, db\_datareader and SQLAgentUserRole permissions to be able to access the data and objects in the MSDB database.   For more information, see [Veeam Backup & Replication Required Permissions](https://helpcenter.veeam.com/docs/vbr/userguide/required_permissions.html?ver=13) and [Veeam ONE Required Permissions](https://helpcenter.veeam.com/docs/one/userguide/connection_to_sql.html?ver=13). |
| NetApp Storage System Permissions | The account used to connect the storage system to Orchestrator must be granted permissions described in section [NetApp Data ONTAP Permissions](#netapp).  Note: Multiple connections to a storage system using different credentials are not supported. |
| HPE Storage System Permissions | The account used to connect the storage system to Orchestrator must be assigned the Super or Edit role. If the account is assigned the Edit role, both the account and the storage resources that you plan to access must belong to the same domain.  Note: Multiple connections to a storage system using different credentials are not supported. |
| Orchestrator Credentials for Application Verification | The account used to run the Verify SharePoint URL step, must be assigned the SharePoint\_Shell\_Access role and must be a member of the WSS\_ADMIN\_WPG group on the processed machine.  The account used to run the Verify Exchange Mailbox step, must be assigned the ApplicationImpersonation role on the processed machine. |

NetApp Data ONTAP Permissions

The account used to connect to a NetApp Data ONTAP storage system must have the following permissions:

NetApp Data ONTAP Permissions

| Command/Directory | Access/Query Level |
| DEFAULT | none |
| job | readonly |
| lun | all |
| network interface | readonly |
| snapmirror | all |
| version | readonly |
| volume | all |
| vserver | readonly |


