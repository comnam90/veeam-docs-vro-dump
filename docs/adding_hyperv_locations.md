---
title: "Adding Microsoft Hyper-V Recovery Locations"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/adding_hyperv_locations.html"
last_updated: "3/12/2026"
product_version: "13.0.0.1167"
---

# Adding Microsoft Hyper-V Recovery Locations


To add a Microsoft Hyper-V or Azure Local recovery location:

1. Switch to the Administration page.
2. Navigate to Recovery Locations.
3. Click Add.
4. Complete the New Recovery Location wizard:

1. [Specify a recovery location name and description](hyperv_location_name.md).
2. [Choose a recovery location type](hyperv_location_type.md).
3. [Specify the connection type of a target cluster](hyperv_location_connection.md).
4. [Choose recovery options](hyperv_location_recovery_options.md).
5. [Choose a target SCVMM server and cluster](hyperv_location_server.md).
6. [Configure network mapping](hyperv_location_network_mapping.md).
7. [Finish working with the wizard](hyperv_location_finish.md).

|  |
| --- |
| Important |
| Before you start adding a Microsoft Hyper-V recovery location, consider the following limitations:   * CSV disks that you plan to use to recover VMs must have the Online status. * All hosts that belong to the cluster where the recovered VMs will reside must be online and available.   Keep in mind that after you bring a Hyper-V object online or perform any infrastructure configuration changes, the changes may not appear in the Orchestrator UI immediately — the data synchronization process between Orchestrator and Microsoft Hyper-V may take up to 2 hours to complete. |


