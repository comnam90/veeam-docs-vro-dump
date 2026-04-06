---
title: "Installing Veeam Recovery Orchestrator in Silent Mode"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/installation_unattended.html"
last_updated: "12/23/2025"
product_version: "13.0.0.1167"
---

# Installing Veeam Recovery Orchestrator in Silent Mode


You can install Orchestrator in the silent automated mode with a special XML answer file using the command line interface. The silent installation mode does not require user interaction — the installation runs automatically in the background, and you do not have to respond to the installation wizard prompts. You can use the silent installation mode to automate the Orchestrator installation process in large-scale environments.

Before You Begin

Before you start silent installation, consider the following:

* The account used to run the silent installation file must be a member of the local Administrators group on the machine where the silent installation will run. The silent installation cannot be run under a LocalSystem or NetworkService account.

* If the account used to run the unattended installation file is logged on to the machine using the network logon method, the unattended installation will fail. To avoid this, use the additional /SkipNetworkLogonErrors command line key.

Installing Veeam Recovery Orchestrator

To install Orchestrator in the silent mode with the answer file, perform the following steps:

1. Copy the VroAnswerFile\_install.xml file to your local drive.

You can find the template answer file on the Orchestrator installation disk in the \Setup\Silent\AnswerFiles\VRO folder. This folder contains the following templates:

* VroAnswerFile\_install.xml — the template for installing Orchestrator
* VroAnswerFile\_uninstall.xml — the template for uninstalling Orchestrator
* VroAnswerFile\_upgrade.xml — the template for upgrading Orchestrator

1. Configure the installation file parameters. For more information on the parameters that you can configure, see section [Silent Installation File Parameters](unattended_installation_server.md).
2. Make sure that the answer file has the correct bundle (Vro) and mode (install):

|  |
| --- |
| <unattendedInstallationConfiguration bundle="Vro" mode="install" version="1.0"> |

1. Start the installation by running the Veeam.Silent.Install.exe file located on the Orchestrator installation disk in the \Setup\Silent folder. To do that, use the following command line keys in your installation command:

|  |
| --- |
| D:\Setup\Silent\Veeam.Silent.Install.exe /AnswerFile E:\MyAnswerFileVROInstall.xml /SkipNetworkLogonErrors |

where:

/AnswerFile — the required key that specifies the path to your custom answer file, for example: E:\MyAnswerFileVROInstall.xml.

/SkipNetworkLogonErrors — the optional key that allows you to skip additional pre-installation validations that may block the silent installation from running.

/LogFolder — the optional key that specifies the path where log files will be saved. By default, Orchestrator uses the C:\ProgramData\Veeam\Setup\Temp folder.


