---
title: "Automatic Usage Reporting"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/automatic_usage_reporting.html"
last_updated: "11/19/2025"
product_version: "13.0.0.1167"
---

# Automatic Usage Reporting


When [automatic license update is enabled](updating_license_automatically.md) for Rental, Subscription and Subscription licenses, Orchestrator additionally performs automatic usage reporting.

As part of reporting, Orchestrator collects statistics on the current license usage and sends it periodically to the Veeam License Update Server. The report provides information on the contract ID, product installation ID, and the maximum number of licensed objects managed by Orchestrator over the past week. The reporting process runs in the background mode, once a week at a random time and day.

The collected data does not include information on Orchestrator usage by any individual person identifiable for Veeam, or any data gathered by Orchestrator. Veeam may also use the collected data for any other internal business purposes it deems appropriate, including (but not limited to) evaluation, improvement and optimization of Veeam licensing models.

By enabling automatic license update, you agree with collection, transmission and use of the reporting data.

|  |
| --- |
| Note |
| For NFR and Evaluation licenses, automatic usage reporting is performed by default and cannot be disabled. |


