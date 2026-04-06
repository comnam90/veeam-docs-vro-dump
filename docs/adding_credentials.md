---
title: "Adding Credentials Parameter to Your Script"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/adding_credentials.html"
last_updated: "1/21/2026"
product_version: "13.0.0.1167"
---

# Adding Credentials Parameter to Your Script


You may add multiple custom parameters of the Credentials type. To pass the credentials to the script, Orchestrator uses the following parameter name convention.

In the script file, a parameter with the Credentials type will split into 2 parameters: the first one will contain a user name and the second one will contain a password. For example, if you add a credential parameter named SQLCreds, Orchestrator will pass it to the script as $SQLCredsUsername and $SQLCredsPassword.

|  |
| --- |
| Param(   [string]$SQLCredsUsername,   [string]$SQLCredsPassword  ) |

|  |
| --- |
| Important |
| The statement must contain a comma-separated list of variables prefixed with a data type. Default values are optional. |


