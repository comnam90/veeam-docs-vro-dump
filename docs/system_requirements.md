---
title: "System Requirements"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/system_requirements.html"
last_updated: "2/12/2026"
product_version: "13.0.0.1167"
---

# System Requirements


The machine where Orchestrator will be deployed must meet the necessary hardware and software requirements, and must have all the [required certificates](https://helpcenter.veeam.com/docs/backup/vsphere/trusted_root_certificates.html?ver=120) installed. In addition to Orchestrator functions, the Orchestrator server can function as a Veeam Backup & Replication server and a Veeam ONE server and, if used in this way, must have sufficient resources provided.

|  |
| --- |
| Important |
| Consider the following limitations:   * Installation of Orchestrator on a machine already running Veeam Backup & Replication or Veeam ONE is not supported.  * Installation of Orchestrator on a machine running Microsoft Windows Server Core is not supported. * Installation of Orchestrator server components in a PostgreSQL database is not supported.  * Installation of Orchestrator server or agent on a machine with the Domain Controller role is not supported.  * Installation of Veeam Backup Enterprise Manager on the same machine that runs the Veeam Orchestrator Server Service is not supported. |

System Requirements

| Specification | Requirement |
| Hardware | Hardware requirements depend on the size of the managed infrastructure. For more information, see [Hardware Recommendations](#hw). |
| OS | Only 64-bit versions of the following operating systems are supported:   * Microsoft Windows Server 2025 * Microsoft Windows Server 2022 * Microsoft Windows Server 2019 * Microsoft Windows Server 2016   Orchestrator can be installed on a Windows Server OS, either domain-joined or in a workgroup. |
| SQL Server | Local and remote installations of the following versions of Microsoft SQL Server are supported:   * Microsoft SQL Server 2022 * Microsoft SQL Server 2019 * Microsoft SQL Server 2017 (2017 SP2 Express Edition is included in the setup) * Microsoft SQL Server 2016   Note: It is not recommended that you use the Express Edition in any production Orchestrator deployments — it should be used for product evaluation only. |
| Veeam Orchestrator Agent | An Orchestrator agent is required to trigger orchestration commands on remote Veeam Backup & Replication servers. The remote Veeam Backup & Replication server must meet the following requirements:   * The server must run Veeam Backup & Replication version 12.3 or later. Note that some new functionality in Orchestrator version 13 will not be available until the remote server is upgraded to version 13.0.1. * The server must be deployed on a Windows Server OS or as a Veeam Software Appliance (either standalone or clustered).   Note: Network address translation (NAT) between the remote Veeam Backup & Replication server and Orchestrator server is not supported. |
| Authentication | Only NTLM authentication is supported. |
| Additional Software | All components will be installed during setup.  For inline editing of report templates, Microsoft Word from Microsoft Office 2010 SP2 or later is required. |
| [Optional] Virtualization Platform | * VMware vSphere 7.0, 8.0, 9.0 * VMware Cloud Director * System Center Virtual Machine Manager (SCVMM) 2022 and 2025 * Hyper-V Windows Server 2022 and 2025 * Azure Local (formerly Azure Stack HCI) 23H2 or later   Notes:   * As direct connections to vSphere hosts are not supported, the Orchestrator server must be connected to VMware vCenter Servers. * The Orchestrator server can be connected either to SCVMM servers, or standalone Hyper-V or Azure Local clusters. * Although Orchestrator can operate in cloud service provider environments, some specific Cloud Connect features may not be supported (for example, Veeam Cloud Connect Replication, importing backups from Veeam Cloud Connect repositories, using VMware Cloud Director as a target recovery location and so on). |
| [Optional] Storage System | * HPE 3PAR 3.3.1, 3.3.2 MU1 * HPE Primera 4.3, 4.4, 4.5 * HPE Alletra 9000 9.3 or later * HPE Alletra MP (B10000) 10.2 or later * NetApp ONTAP 9.10, 9.11, 9.12, 9.13, 9.14, 9.15, 9.16, 9.17 * Lenovo DM/DG Series 9.10, 9.11, 9.12, 9.13, 9.14, 9.15, 9.16, 9.17   Notes:   * Orchestrated failover of volumes protected by SnapMirror synchronous replication is not supported for NetApp ONTAP version 9.12 or later. * Orchestrated failover of Consistency Groups (CG) protected by SnapMirror asynchronous replication is not supported for NetApp ONTAP 9.12 or later. * Orchestrated failover of volumes protected using SnapVault is not supported. * Orchestrated failover of SVMs protected using SnapMirror is not supported. |

Hardware Recommendations

Hardware Recommendations

| Number of Protected Systems\* | 1–1500 | 1500–5000 | 5000–10000 | 10000–20000+ |
| CPU | 8 vCPUs for the Orchestrator server  4 vCPUs – 8 vCPUs for the Microsoft SQL Server | 10 vCPUs for the Orchestrator server  10 vCPUs for the Microsoft SQL Server | 12 vCPUs for the Orchestrator server  12 vCPUs for the Microsoft SQL Server | >20 vCPUs for the Orchestrator server  >20 vCPUs for the Microsoft SQL Server |
| Memory | 12 GB for the Orchestrator server  8 GB for the Microsoft SQL Server | 40 GB for the Orchestrator server  40 GB for the Microsoft SQL Server | 70 GB for the Orchestrator server  70 GB for the Microsoft SQL Server | >70 GB for the Orchestrator server  >70 GB for the Microsoft SQL Server |
| SQL Server | N/A | N/A | Disk IOPS 1000 (minimum) | Disk IOPS 2000 (minimum) |
| Hard Disk Space | 30 GB for product installation and sufficient disk space for the Veeam ONE database (if installed locally). Use the [Veeam ONE Database Calculator](https://www.veeam.com/kb2246) to size application data.  20 GB for the Microsoft SQL Server. By default, the Microsoft SQL Server database grows as follows:   * ~1 Mb per one Readiness Check Report or Plan Execution Report for a plan that includes 10 machines. * ~10 Mb per one Readiness Check Report or Plan Execution Report for a plan that includes 100 machines. * ~100 Mb per one Readiness Check Report or Plan Execution Report for a plan that includes 1000 machines.   Note: SSD disks are recommended to use with the Microsoft SQL Server. | | | |

\*The total number of systems protected by replicas and backups (including Veeam agent and VMware vSphere VM backups). Assumes one restore point per system per day.


