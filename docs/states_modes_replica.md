---
title: "Plan States and Modes"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/states_modes_replica.html"
last_updated: "1/12/2026"
product_version: "13.0.0.1167"
---

# Plan States and Modes


Replica plans can acquire the following default states after creation. The same states are shown after resetting a plan, and after completing a test or a check.

Plan States and Modes

| Plan State | Icon | Description |
| NEEDS VERIFIED | ![Plan States and Modes](images/plan_notverified.webp) | Plan has never been tested, has never passed a readiness check, or has been changed since the last DataLab test or readiness check. |
| NOT VERIFIED | ![Plan States and Modes](images/plan_verificationfailed.webp) | Plan has failed to be tested or has failed to pass a readiness check or malware scan. |
| VERIFIED | ![Plan States and Modes](images/plan_verified.webp) | Plan has been tested successfully or has passed a readiness check or malware scan. |

Replica plans can acquire the following stable states after completing current processing:

Plan States and Modes

| Plan State | Icon | Description |
| HALTED | ![Plan States and Modes](images/plan_halted.webp) | Plan has stopped due to either an error or user intervention. |
| FAILOVER  UNDO FAILOVER  PERMANENT FAILOVER  PREPARE FOR FAILBACK  FAILBACK  UNDO FAILBACK  COMMIT FAILBACK | ![Plan States and Modes](images/plan_complete.webp) | Process completed successfully. |
| ![Plan States and Modes](images/state_warning.webp) | Process completed with one or more warnings. |
| ![Plan States and Modes](images/state_error.webp) | Process completed with one or more errors. |
| TESTING HALTED | ![Plan States and Modes](images/halted_test.webp) | Plan testing has stopped due to either an error or user intervention. |

Replica plans can acquire the following active states while in use or in progress:

Plan States and Modes

| Plan State | Icon | Description |
| Plan Management | | |
| CREATING | ![Plan States and Modes](images/plan_editing.webp) | Plan is being created. |
| EDITING | ![Plan States and Modes](images/plan_editing.webp) | Plan is being edited. |
| SAVING | ![Plan States and Modes](images/plan_saving.webp) | Plan is being saved. |
| RESETTING | ![Plan States and Modes](images/plan_resetting.webp) | Plan is being reset. |
| DELETING | ![Plan States and Modes](images/plan_deleting.webp) | Plan is being deleted. |
| Readiness Checks | | |
| CHECKING | ![Plan States and Modes](images/plan_rc.webp) | Plan readiness check is in progress. |
| ![Plan States and Modes](images/readiness_check_warning.webp) | Plan readiness check is in progress; one or more warnings encountered. |
| ![Plan States and Modes](images/readiness_check_error.webp) | Plan readiness check is in progress; one or more errors encountered. |
| CHECK HALTING | ![Plan States and Modes](images/plan_halting.webp) | Plan readiness check is halting. |
| Execution, Testing and Scanning | | |
| FAILOVER | ![Plan States and Modes](images/plan_processing.webp) | Plan is executing. |
| ![Plan States and Modes](images/state_warning.webp) | Plan is executing; one or more warnings encountered. |
| ![Plan States and Modes](images/state_error.webp) | Plan is executing; one or more errors encountered. |
| HALTING | ![Plan States and Modes](images/plan_halting.webp) | Plan is halting. |
| TEST PENDING | ![Plan States and Modes](images/test_pending.webp) | Plan is waiting for the DataLab to power on. |
| TESTING | ![Plan States and Modes](images/test_progress.webp) | Plan testing is in progress. |
| ![Plan States and Modes](images/test_warning.webp) | Plan testing is in progress; one or more warnings encountered. |
| ![Plan States and Modes](images/test_errors.webp) | Plan testing is in progress; one or more errors encountered. |
| TEST HALTING | ![Plan States and Modes](images/test_halting.webp) | Plan testing is halting. |
| POWERING OFF | ![Plan States and Modes](images/power_off.webp) | Plan testing is being powered off. |
| SCAN | ![Plan States and Modes](images/scan_icon.webp) | Plan scanning for malware is in progress. |

|  |
| --- |
| Note |
| If you perform any infrastructure configuration changes (add, delete or rename VMs) or changes to Veeam ONE Business View groups, Orchestrator will not automatically apply these changes to plans that are currently being executed or tested — such plans are ‘locked’ and cannot be edited. The changes will take effect only if the plans enter the VERIFIED, NEEDS VERIFIED or NOT VERIFIED state. |

Replica plans can acquire the following modes:

Plan States and Modes

| Plan Mode | Icon | Description |
| ENABLED | ![Plan States and Modes](images/plan_enabled.webp) | Plan is ready to be verified, tested, scanned and executed.  Notes: |
| DISABLED | ![Plan States and Modes](images/plan_disabled.webp) | Plan is ready to be edited, tested and scanned.  Notes:  Scheduled plan execution is not available. Automatic report updates are disabled. |
| IN-USE | ![Plan States and Modes](images/plan_in_use.webp) | Plan is either in one of the active states (except the EDITING state) or in one of the stable states.  Notes: Plan editing is not available. Automatic report updates are disabled. |


