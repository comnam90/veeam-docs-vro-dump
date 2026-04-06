---
title: "Adding Recovery Locations"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/adding_recovery_locations.html"
last_updated: "11/24/2025"
product_version: "13.0.0.1167"
---

# Adding Recovery Locations


All resource groups created based on vCenter Server tags will automatically become available for the creation of recovery locations in the Orchestrator UI. However, after you assign a tag to an object in the vSphere inventory, the object may not be available in the Orchestrator UI immediately — the data synchronization process between Orchestrator and Veeam ONE occurs every 3 hours.

|  |
| --- |
| Tip |
| You can speed up the data synchronization process using Veeam ONE Reporter installed as part of the embedded Veeam ONE server. To do that:   1. In a web browser, navigate to the Veeam ONE Reporter web address.   The address consists of an FQDN of the Orchestrator server and the website port specified during installation (by default, 1239). Note that Veeam ONE Reporter is available over HTTPS.  https://<FQDN>:1239/   1. Switch to the Configuration page. 2. Navigate to Data Collection. 3. From the Advanced Actions menu, select Start report data collection. |

To add a recovery location to be used when performing a failback operation, follow the instructions provided in section [Adding VMware vSphere Recovery Locations](adding_restore_locations.md). To add a recovery location to be used when running a restore plan, follow the instructions provided in sections [Adding VMware vSphere Recovery Locations](adding_restore_locations.md) and [Adding Microsoft Hyper-V Recovery Locations](adding_hyperv_locations.md). To add a recovery location to be used when running a storage plan, follow the instructions provided in section [Adding Storage Recovery Locations](adding_storage_locations.md). To add a recovery location to be used when running a cloud plan, follow the instructions provided in section [Adding Microsoft Azure Recovery Locations](adding_cloud_locations.md).


