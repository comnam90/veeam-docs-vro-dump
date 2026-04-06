---
title: "Ports"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/ports.html"
last_updated: "2/12/2026"
product_version: "13.0.0.1167"
---

# Ports


The following table lists typical connection settings required for Orchestrator components.

|  |
| --- |
| Note |
| These requirements assume that the embedded Veeam Backup & Replication and Veeam ONE components are used only in the default configuration (to support Orchestrator activities), and not for full production functionality.  If the embedded Orchestrator components are used for additional functionality, see the Veeam Backup & Replication User Guide, section [Ports](https://helpcenter.veeam.com/docs/vbr/userguide/used_ports.html?ver=13) and Veeam ONE Deployment Guide, section [Ports](https://helpcenter.veeam.com/docs/one/userguide/ports.html?ver=13) for the full requirements. |

Ports

| From | To | Protocol | Port | Notes |
| Orchestrator server | vCenter Server | TCP/HTTPS | 443 | Used by the embedded Veeam Backup & Replication and Veeam ONE servers to connect to the vCenter Server. |
| SVM (NetApp) | HTTPS | 443 | Used by the Veeam Orchestrator Server Service to access the management interface of the storage virtual machine. |
| Storage system (HPE) | HTTPS | 443 | Used by the Veeam Orchestrator Server Service to connect to the HPE Primera storage system. |
| HTTPS | 8080 | Used by the Veeam Orchestrator Server Service to connect to the HPE 3PAR storage system. |
| Microsoft SQL Server | TCP | 1433 | Required to provide access to the Microsoft SQL Server where Orchestrator, embedded Veeam Backup & Replication and ONE databases are stored.  Additional ports may need to be open depending on your configuration. For more information, see [Microsoft Docs](https://msdn.microsoft.com/en-us/library/cc646023%28v%3Dsql.120%29.aspx#BKMK_ssde). |
| Veeam Backup & Replication server (Microsoft Windows) | TCP | 135; 445 | Required to deploy Orchestrator agents to remote Veeam Backup & Replication servers. |
| Veeam Backup & Replication server | TCP | 443 | Used by the Veeam Orchestrator Server Service to connect to remote Veeam Backup & Replication servers. |
| TCP | 49152 to 65535 | Dynamic RPC port range for Microsoft Windows 2008 and later. For more information, see this [Microsoft KB article](https://support.microsoft.com/kb/929851/en-us).  Note: If you use the default Microsoft Windows firewall settings, you do not need to configure dynamic RPC ports. During setup, Orchestrator automatically creates a firewall rule for the runtime process. However, If you use custom firewall settings or encounter the "RPC function call failed" error during the application-aware processing, you will need to configure dynamic RPC ports. For more information on how to configure RPC dynamic port allocation to work with firewalls, see this [Microsoft KB article](https://support.microsoft.com/en-us/help/154596/how-to-configure-rpc-dynamic-port-allocation-to-work-with-firewalls). |
| Veeam Backup Enterprise Manager server | HTTPS | 50001 | Used by the Veeam Orchestrator Server Service to detect Veeam Backup & Replication servers running on Veeam Enterprise Manager servers. |
| Veeam Backup & Replication server | Orchestrator server | HTTPS | 8888 | Required to deploy Orchestrator agents to remote Veeam Backup & Replication servers. Then, this port is used by the Veeam Orchestrator Server Service to connect to the Orchestrator agents running on these servers. |
| Orchestrator server | TCP | 443 | Used by remote Veeam Backup & Replication severs to connect to Orchestrator agents. |
| vSphere VM guest OS | TCP | Ports for VM guest OS connection | Required to run in-guest scripts on a virtual machine being tested, failed over or restored.  For the full list of ports that must be opened to ensure proper communication of the Veeam Backup & Replication server with the runtime coordination process deployed inside the VM guest OS, see the Veeam Backup & Replication User Guide, section [Ports](https://helpcenter.veeam.com/docs/vbr/userguide/used_ports.html?ver=13).  Make sure that the VM is configured to allow inbound traffic: the default File and Printer Sharing (SMB-In) firewall rule must be enabled. |
| Workstation web browser | Veeam ONE Reporter Web UI | HTTPS | 1239 | Required to access the Veeam ONE Reporter console from a user workstation. |
| Orchestrator UI | Orchestrator server | TCP | 12348 | Used by the Orchestrator UI to connect to the remote Veeam Orchestrator Server Service. |
| Orchestrator UI | Orchestrator server | HTTPS | 9898 | Required to access the Veeam Orchestrator Web UI from a user workstation. |
| Veeam ONE Client | Orchestrator server | TCP | 139; 445 | Used by Veeam ONE Client to communicate with the embedded Veeam ONE server. |
| Veeam Backup Catalog service | Veeam Backup & Replication server | TCP | 9393 | Required to collect indexing data for backup and replication jobs, and to store this data in the Veeam Backup Catalog folder on the Veeam Backup & Replication server. |
| Veeam Backup & Replication console | Veeam Backup & Replication server | TCP | 9392 | Used by the Veeam Backup & Replication console to connect to the Veeam Backup & Replication server. |
| Veeam backup source connection | Veeam Backup & Replication server | TCP | 9401 | Used by the mount server to communicate with the Veeam Backup & Replication server. |
| Veeam License Update Server | Orchestrator server | TCP | 443 | Required to get automatic license updates. |


