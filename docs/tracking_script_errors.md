---
title: "Capturing Script Errors and Warnings"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/tracking_script_errors.html"
last_updated: "1/21/2026"
product_version: "13.0.0.1167"
---

# Capturing Script Errors and Warnings


To log any custom script information into step details and execution reports, make sure to use the [Write-Host](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/write-host?view=powershell-5.1) cmdlet in the script. To indicate errors and warnings occurred during script execution and to pass this data to Orchestrator, make sure to use the [Write-Error](https://technet.microsoft.com/en-us/library/hh849962.aspx) and [Write-Warning](https://technet.microsoft.com/en-us/library/hh849931.aspx) cmdlets in the script. This will post script output in the Orchestrator UI, and also in [Plan Execution](viewing_plan_execution_history.md) and [DataLab Test](viewing_test_execution_history.md) reports.

If no errors and warnings occur during script execution, Orchestrator will report the Success execution state. Otherwise, in case a number of warnings and errors occurs, Orchestrator will report the worst state.

|  |
| --- |
| Note |
| For a script that runs inside the guest OS of a machine included in a cloud plan, the Write-Warning cmdlet is not supported. |


