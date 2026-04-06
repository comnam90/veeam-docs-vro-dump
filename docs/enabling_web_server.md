---
title: "Enabling HPE 3PAR Web Services API Server"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/enabling_web_server.html"
last_updated: "2/26/2024"
product_version: "13.0.0.1167"
---

# Enabling HPE 3PAR Web Services API Server


Orchestrator uses the HPE 3PAR Web Services API (WSAPI) server to communicate with HPE Primera and HPE 3PAR storage systems. When you add an HPE Primera or HPE 3PAR storage system to Orchestrator, it does not enable the WSAPI server automatically because it does not have enough privileges to perform this operation. This means that you must enable the server manually before connecting the storage system to Orchestrator.

To enable the WSAPI server running on an HPE Primera or HPE 3PAR storage system:

1. Log on to the Processor with administrator privileges:

|  |
| --- |
| #ssh <administrator account>@<SP IP Address> |

1. Run the following command to view the current state of the WSAPI server:

|  |
| --- |
| #showwsapi  -- -State- -HTTP\_State-  HTTP\_Port -HTTPS\_State- HTTPS\_Port -Version-  Enabled   Active Enabled       8008  Enabled       8080         1.1 |

1. If the WSAPI server is not running, run the following command to start it:

|  |
| --- |
| #startwsapi |

If the HTTPS port is disabled, run the following command to enable it:

|  |
| --- |
| #setwsapi -https enable |


