---
title: "Installing Veeam Recovery Orchestrator"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/installation_procedure.html"
last_updated: "2/11/2026"
product_version: "13.0.0.1167"
---

# Installing Veeam Recovery Orchestrator


During Orchestrator installation, Orchestrator server components will be installed all together on a single machine. For more information on the components, see [Solution Architecture](https://helpcenter.veeam.com/docs/vro/userguide/solution_architecture.html?ver=13).

|  |
| --- |
| Important |
| When installing Orchestrator, consider the following limitations:   * Installation of Orchestrator on a machine already running Veeam Backup & Replication or Veeam ONE is not supported. The embedded Veeam Backup & Replication and Veeam ONE components are co-installed with the Orchestrator server. * Installation of Orchestrator server or agent on a machine with the Domain Controller role is not supported. |

To install Orchestrator, perform the following steps:

1. [Launch the splash window](launch_splash_window.md).
2. [Start the setup wizard](start_setup.md).
3. [Accept the license agreement](accept_license_agreement.md).
4. [Review components to install](choose_components.md).
5. [Provide a license file](provide_license_file.md).
6. [Specify service account credentials](specify_service_credentials.md).
7. [Choose a SQL server](choose_sql_server.md).
8. [Perform system configuration check](perform_configuration_check.md).
9. [Choose a PostgreSQL server](choose_postgresql_server.md).
10. [Create SQL server databases](create_sql_databases.md).
11. [Specify data locations](specify_data_location.md).
12. [Specify service ports](specify_service_ports.md).
13. [Select a certificate for the Orchestrator UI](select_vro_certificate.md).
14. [Review installation summary](review_advanced_summary.md).
15. [Upgrade to Veeam Backup & Replication 13](install_vbr.md)

Before You Begin

Before you begin installation, check the following prerequisites:

1. Make sure the machine where Orchestrator will be installed meets the prerequisite conditions described in section [System Requirements](system_requirements.md).
2. Download the product installation file VeeamDataPlatform\_[date].iso from the [Veeam downloads page](https://www.veeam.com/downloads.html). You can burn the downloaded image file to a CD/DVD or mount the installation image to the target machine using disk image emulation software.


