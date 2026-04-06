---
title: "Editing Original VM Location"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/configuring_original_recovery_location.html"
last_updated: "1/20/2026"
product_version: "13.0.0.1167"
---

# Editing Original VM Location


Since all resource groups included in the Original VM Location are empty by default and depend on processed machines, you cannot customize its resource settings. However, you can still customize some general settings for the location:

1. Switch to the Administration page.
2. Navigate to Recovery Locations.
3. In the list of recovery locations, select Original VM Location, and click Edit.
4. Complete the Edit Recovery Location wizard:

1. To change the configured recovery options, follow the instructions provided in section [Adding VMware vSphere Recovery Locations](restore_location_recovery_options.md) (step 3).

[![Editing Original Recovery Location](images/configuring_original_location_options.webp)](images/configuring_original_location_options.webp "Editing Original Recovery Location")

1. To change the datastore capacity level that must not be breached during the recovery process, follow the instructions provided in section [Adding VMware vSphere Recovery Locations](restore_location_recovery_options.md) (step 3).

[![Editing Original Recovery Location](images/configuring_original_location_vsphere.webp)](images/configuring_original_location_vsphere.webp "Editing Original Recovery Location")

1. At the Summary step of the wizard, review configuration information and click Finish to confirm the changes.

[![Editing Original Recovery Location](images/configuring_original_location_finish.webp)](images/configuring_original_location_finish.webp "Editing Original Recovery Location")


