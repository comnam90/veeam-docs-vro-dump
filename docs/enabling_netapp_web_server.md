---
title: "Enabling NetApp ONTAP API"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/enabling_netapp_web_server.html"
last_updated: "5/4/2026"
product_version: "13.0.0.1167"
---

# Enabling NetApp ONTAP API


Orchestrator uses the NetApp ONTAP API (ZAPI) to communicate with NetApp storage systems. When you add a NetApp storage system to Orchestrator, it does not enable the ZAPI automatically because it does not have enough privileges to perform this operation. This means that you must enable the API manually before connecting the storage system to Orchestrator.

To enable the ZAPI, do the following

1. Connect to the system through SSH.
2. Run the following command:

|  |
| --- |
| vserver services web modify -vserver <svm-name> -name ontapi -enabled true |

-OR-

Send the following ONTAP REST API request

|  |
| --- |
| PATCH https://<cluster-ip>/api/private/cli/vserver/services/web?vserver=<svm-name>&name=ontapi  { "enabled": true } |


