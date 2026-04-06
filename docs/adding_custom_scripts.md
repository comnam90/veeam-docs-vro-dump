---
title: "Managing Custom Scripts to Veeam Recovery Orchestrator"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/adding_custom_scripts.html"
last_updated: "1/21/2026"
product_version: "13.0.0.1167"
---

# Managing Custom Scripts to Veeam Recovery Orchestrator


If you have a PowerShell script that you want to run as part of the recovery process, you can upload your script into Orchestrator, and it will be executed when you run your plan.

The script can run on a Veeam Backup & Replication server, on the Orchestrator server or inside each machine included in the plan. You can customize settings required for script execution and pass various parameters into the script: credentials, runtime variables (such as vm\_name or plan\_state) and any other custom parameters you require. Script output will be captured in plan details in the Orchestrator UI, and in [Plan Execution](viewing_plan_execution_history.md) and [DataLab Test](viewing_test_execution_history.md) reports.

|  |
| --- |
| Note |
| Due to [Microsoft Azure limitations](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/run-command), script output for cloud plans is limited to 4 Kb. |

Requirements

If you want to create a custom script and execute it when running a recovery plan, you must take into account the following considerations.

* Running custom scripts inside guest OSes of Linux-based machines is not supported.
* The script you want to use must be a PowerShell script. Orchestrator 13 supports PowerShell scripts only.
* To allow the script to run inside a machine guest OS, it is required that you have Microsoft PowerShell 3.0 and .Net Framework 4.0 installed on each machine for which you enable the custom script step.
* To allow the script to run inside the guest OS of a machine recovered to Microsoft Azure, the client secret or certificate must be specified for the Microsoft Azure account added to the Veeam Backup & Replication protecting this machine. For more information, see [Connecting Microsoft Azure Servers](connecting_azure_servers.md).
* To allow the script to run inside the guest OS of a machine recovered to Microsoft Azure, the compute account (Azure AD application) added to the Veeam Backup & Replication server configuration and used to access the Microsoft Azure resources must be assigned the Contributor and Key Vault Crypto User user roles. Alternatively, you can create a custom role on the Microsoft Azure portal with the granular permissions listed in the Veeam Backup & Replication User Guide, section [Creating Custom Role for Azure and Azure Stack Hub Accounts](https://helpcenter.veeam.com/docs/vbr/userguide/azure_custom_role.html?ver=13#permissions-for-azure-compute-account--existing-application-). Note that this role must also have the following permissions assigned: Microsoft.Compute/virtualMachines/runCommands/read, Microsoft.Compute/virtualMachines/runCommands/write, Microsoft.Compute/virtualMachines/runCommands/delete.
* To allow the script to run on a Veeam Backup & Replication server, no additional software is required.

In This Section

* [Adding Custom Scripts](uploading_scripts.md)
* [Configuring Common Parameters](script_common_parameters.md)
* [Configuring Windows Credentials Parameter in Orchestrator UI](customizing_credentials.md)
* [Adding Credentials Parameter to Your Script](adding_credentials.md)
* [Using Runtime Parameter Variables](using_parameter_variables.md)
* [Adding Custom Script Step to Plan](adding_custom_step.md)
* [Capturing Script Errors and Warnings](tracking_script_errors.md)


