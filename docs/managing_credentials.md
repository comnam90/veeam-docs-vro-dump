---
title: "Managing Credentials"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/managing_credentials.html"
last_updated: "1/20/2026"
product_version: "13.0.0.1167"
---

# Managing Credentials


Orchestrator Administrators can choose which credentials will be visible to Plan Authors and available for use in recovery plans. These credentials can be used in plans, for example, to run verification scripts inside the guest OS, or in other checks.

The Orchestrator UI allows you to [edit the existing credentials](changing_passwords.md), and [add any domain and non-domain accounts](adding_credentials_manually.md).

|  |
| --- |
| Important |
| Starting from Orchestrator version 13, credentials from the Orchestrator UI are not synchronized into the Veeam Backup & Replication console. This means that if you change a password in the Orchestrator UI, you must also update this password manually in the Veeam Backup & Replication console as described in the Veeam Backup & Replication User Guide, section [Managing Credentials](https://helpcenter.veeam.com/docs/vbr/userguide/managing_credentials.html?ver=13). |


