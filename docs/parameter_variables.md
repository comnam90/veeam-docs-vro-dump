---
title: "Parameter Variables"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/parameter_variables.html"
last_updated: "2/24/2025"
product_version: "13.0.0.1167"
---

# Parameter Variables


Parameter variables are passed between steps during plan execution, and are available when editing and adding step parameters.

You can define the following variables for any step parameter that allows plain text to be entered:

Parameter Variables

| Parameter Variable | Content |
| %vm\_fqdn% | FQDN of the currently processed machine |
| %current\_vm\_ip% | IP address of the currently processed VM |
| %current\_vm\_name% | Name of the currently processed VM |
| %current\_vm\_ip\_list% | All IP addresses of the currently processed VM |
| %target\_vm\_ip% | IP address of the target VM |
| %target\_vm\_ip\_list% | All IP addresses of the target VM |
| %target\_vm\_name% | Name of the target VM |
| %replica\_vm\_state% | State of the currently processed replica VM |
| %source\_machine\_name% | Name of the source machine |
| %source\_vm\_ip% | IP address of the source VM |
| %source\_vm\_ip\_list% | All IP addresses of the source VM |
| %source\_vm\_name% | Name of the source VM |
| %plan\_name% | Name of the recovery plan |
| %vao\_server\_name% | Name of the Orchestrator server |
| %plan\_state% | Current state of the recovery plan |
| %plan\_test\_mode% | Boolean variable that indicates whether the plan is currently being tested (True/False) |
| %group\_name% | Name of the currently processed inventory group |
| %plan\_summary% | Output information on the recovery plan (error/warning/success for all steps) |
| %group\_summary% | Output information on the currently processed inventory group |
| %vm\_summary% | Output information on the currently processed VM |
| %vao\_ui% | URL to access the home page of the Orchestrator UI |
| %plan\_vms% | List of all machines included in the recovery plan |


