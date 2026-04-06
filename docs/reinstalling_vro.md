---
title: "Reinstalling Orchestrator Using Existing Databases"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/reinstalling_vro.html"
last_updated: "3/12/2026"
product_version: "13.0.0.1167"
---

# Reinstalling Orchestrator Using Existing Databases


In some cases, you may need to migrate the Orchestrator server to another machine or reinstall it using existing databases. To do that, follow the instructions provided in this section.

|  |
| --- |
| Important |
| Before you reinstall Orchestrator, it is required that you disable multi-factor authentication. Otherwise, you will not be able to log in to the Web UI. For more information on how to disable MFA, see [Enabling and Disabling Multi-Factoring Authentication](enabling_mfa.md). |

Step 1. Back Up Existing Databases

Before you reinstall Orchestrator, you must create backups of databases used to store data collected from Orchestrator, Veeam Backup & Replication and Veeam ONE, which were previously installed with the Orchestrator server.

You must also create a backup of the registry key used to encrypt and decrypt credentials stored in the Orchestrator database. To do that, open the Windows Registry Editor and export the HKEY\_LOCAL\_MACHINE\SOFTWARE\Veeam\Availability Orchestrator\Server\Security folder.

Step 2. Restore Backed-Up Databases

Restore the backed-up Orchestrator, Veeam Backup & Replication and Veeam ONE databases to a new local or remote Microsoft SQL Server instance.

|  |
| --- |
| Important |
| It is required that the restored databases are located on the same Microsoft SQL Server instance and have the same names as the previously installed databases. |

Step 3. Install Veeam Recovery Orchestrator

Run the Orchestrator setup wizard and follow the instructions provided in section [Deploying Veeam Recovery Orchestrator](installation_procedure.md).

|  |
| --- |
| Important |
| It is required that you install the same Orchestrator version as the previously installed one. |

At the Database Names step of the wizard, browse to the restored Orchestrator database, and specify names to create new Veeam Backup & Replication and Veeam ONE databases.

|  |
| --- |
| Note |
| Orchestrator reinstallation process does not involve the Veeam Backup & Replication and Veeam ONE databases that you restored at step 2. To allow Orchestrator to use the restored databases, you must perform reconfiguration of Veeam ONE and Veeam Backup & Replication servers as described at step 4. |

Step 4. Reconfigure Veeam ONE and Veeam Backup & Replication

As soon as the Orchestrator installation process completes:

1. Open the Services snap-in and stop the Veeam Orchestrator Server Service, Veeam Orchestrator ONE Integration Service and Veeam Orchestrator Agent for Backup service.
2. Reconfigure Veeam ONE and Veeam Backup & Replication servers to use old databases instead of new ones created during Orchestrator installation.

For more information, see these Veeam KB articles: [Moving Veeam ONE database to a different SQL Server](https://www.veeam.com/kb1599) and [How to move the Veeam Backup & Replication software to another server](https://www.veeam.com/kb1889).

1. Import the folder that you exported at [step 1](#step1) to a new machine where Orchestrator is installed, double-click the imported vro registry key file and click Yes in the Registry Editor confirmation window.

As soon as you confirm the operation, the key will be imported to the Windows registry of the new machine.

1. Start the Veeam Orchestrator Server Service, Veeam Orchestrator ONE Integration Service and Veeam Orchestrator Agent for Backup service.

Step 5. Additional Configuration

Depending on the new database location, you will have to perform a number of additional actions.

Installing Orchestrator on the same machine

If you have performed installation on the same machine that was used to run Orchestrator earlier, no additional configuration is required.

Installing Orchestrator on a new machine with the same name

If you have performed installation on a new machine with the same name as the machine that was used to run Orchestrator earlier, do the following.

1. Open the Orchestrator UI and switch to the Administration page.
2. Navigate to Credentials.

Modify all manually added credentials managed by the Orchestrator server.

1. Select a credential and click Edit.
2. In the Edit Credentials window, enter a password for the credential.
3. Repeat the step for each manually added credential.

|  |
| --- |
| Note |
| All credentials collected from remote Veeam Backup & Replication servers will be automatically updated as soon as Orchestrator agents installed on the servers connect to the Orchestrator server. |

1. Navigate to Infrastructure > Orchestrator Agents and make sure that all Orchestrator agents previously installed on the server have the Healthy status.
2. Navigate to Infrastructure > VMware and make sure that all VMware servers previously connected to the server have the Connected status.
3. Navigate to Infrastructure > Microsoft and make sure that all SCVMM servers previously connected to the server have the Connected status.
4. Navigate to Infrastructure > Storage and make sure that all storage systems previously connected to the server have the Connected status.
5. Navigate to Infrastructure > Azure and make sure that all Orchestrator agents previously installed on the server with connected Microsoft Azure accounts have the Connected status.

1. [Applies only if you have previously connected an SMTP server and enabled authorization]

Navigate to Mail.

1. Click Edit.
2. In the SMTP Server window, enter a password required for SMTP server authentication.

Installing Orchestrator on a new machine with a new name

If you have performed installation on a new machine with a new name, follow the instructions provided in [steps 1–8](#new_machine). No additional actions are required.

|  |
| --- |
| Tip |
| To make sure all the configuration changes are correct, after you perform the required actions, generate the Plan Readiness Check Report for each Orchestrator plan. For more information on the report, see [Running Plan Readiness Check](running_readiness_check.md). |


