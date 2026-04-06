---
title: "Licensed Objects"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/licensed_objects.html"
last_updated: "12/12/2025"
product_version: "13.0.0.1167"
---

# Licensed Objects


To work with Orchestrator, you will require licenses for objects to be orchestrated by the solution (backups or replicas of virtual or physical machines) and for the managed Veeam environment (Veeam Backup & Replication and Veeam ONE). This section describes how these managed objects are licensed, and what types of licenses you will need to obtain.

Licensing for Orchestrated Objects

Each machine processed by a recovery plan requires a license. A license here is a unit (or token) that is assigned to a machine to make it manageable in Orchestrator. In version 13, each machine consumes one license instance regardless of the number of plans and DataLabs that include the machine.

|  |
| --- |
| Note |
| All machines added to the plan consume license instances, even if they have no replica or backup. All machines used in DataLab groups to support plan testing environments also consume license instances. |

Licensing for Remote Veeam Backup & Replication Servers with Orchestrator Agents

Each remote Veeam Backup & Replication server connected to Orchestrator must have the Enterprise or Enterprise PLUS edition installed. Otherwise, Orchestrator will not be able to deploy its agent on the server.

|  |
| --- |
| Important |
| * Connections to Veeam Backup & Replication servers with the Essentials pack license are not supported. * Connections to Veeam Backup & Replication servers with the NFR license are supported only if the Orchestrator server has the NFR license installed. |

Edition check is the only check made by Orchestrator to verify licensing of remote Veeam Backup & Replication servers. All operations with licenses on remote Veeam Backup & Replication servers are accomplished according to the Veeam Backup & Replication guidelines. For more information on Veeam Backup & Replication licensing, see the Veeam Backup & Replication User Guide, section [Licensing](https://helpcenter.veeam.com/docs/vbr/userguide/licensing.html?ver=13).

Licensing for Embedded Veeam Backup & Replication and Veeam ONE Servers

Orchestrator is always installed with the other components of the Veeam Data Platform (VDP) — Veeam Backup & Replication and Veeam ONE. The license file is a VDP Premium license that also licenses the embedded components.


