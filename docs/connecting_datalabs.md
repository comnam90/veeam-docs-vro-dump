---
title: "Connecting DataLabs"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/connecting_datalabs.html"
last_updated: "10/20/2025"
product_version: "13.0.0.1167"
---

# Connecting DataLabs


To validate your disaster recovery plans without impacting the production infrastructure, you can configure automatic scheduled testing for the verification of vSphere and agent backups, VM replicas, applications and storage snapshots. For this purpose, Orchestrator uses virtual labs created in the Veeam Backup & Replication console. These virtual labs provide an isolated environment in which Orchestrator performs verification tests.

After you [create a virtual lab](https://helpcenter.veeam.com/docs/vbr/userguide/virtual_lab.html?ver=13) on a Veeam Backup & Replication server connected to your Orchestrator server, you must configure a connection to the VMware Server used to manage the lab, as described in section [Connecting VMware vSphere Servers](connecting_vsphere_servers.md). Otherwise, Orchestrator will not be able to discover the virtual lab and make it available in the Orchestrator UI. Note that the data synchronization process between Orchestrator and the Veeam Backup & Replication server may take several minutes to complete.

|  |
| --- |
| Note |
| Virtual labs created in Veeam Backup & Replication are referred to as DataLabs in Orchestrator. |


