---
title: "New VMs (Rental Licenses)"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/new_vms.html"
last_updated: "11/17/2023"
product_version: "13.0.0.1167"
---

# New VMs (Rental Licenses)


To provide more flexibility and introduce a trial period for machine recovery, Orchestrator offers the concept of New VMs. New VMs are machines that were discovered by Orchestrator within the current calendar month. This mechanism is provided for Rental licenses only.

New machines are managed by Orchestrator as regular machines, but they do not consume licenses until the beginning of the new month. In license terms, New VMs are counted separately from regular managed machines. However, such machines do participate in all Orchestrator activities and are fully functional.

On the first day of the new month, the number of New VMs introduced in the previous month is added to the number of regular managed machines. Machines that were treated as New will be managed by Orchestrator in the following cases:

* If there are enough Orchestrator licenses to allocate to these machines.
* If there are no Orchestrator licenses, but the allowed increase limit has not been breached yet. In this case, the machines will obtain the Licensed by exceed status.

If the allowed increase limit has been already surpassed, these machines will obtain the Unlicensed status.


