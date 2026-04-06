---
title: "Verify SQL Database"
product: "vro"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vro/userguide/verify_sql_database.html"
last_updated: "1/8/2026"
product_version: "13.0.0.1167"
---

# Verify SQL Database


This step verifies the SQL database instance accessibility.

|  |
| --- |
| Important |
| 1. To allow the script to run inside the guest OS of a processed machine, it is required that you have Microsoft PowerShell 3.0, .Net Framework 4.0 and SQL Server 2008 (or later) installed on each machine for which you enable this step. 2. To allow the script to verify the SQL database instance accessibility, the verified SQL Server instance must run Microsoft Windows Server 2008 R2 (or later). 3. To allow the script to connect to the verified SQL Server instance, Orchestrator uses an account whose credentials are specified as values for either the [Windows Credentials](#wincreds) or [SQL Credentials](#sqlcreds) parameter. The account must have the VIEW ANY DATABASE permission. For more information, see [Microsoft Docs](https://docs.microsoft.com/en-us/sql/relational-databases/system-catalog-views/sys-databases-transact-sql#permissions). |

You can override the following parameters for the Verify SQL Database step:

Verify SQL Database

| Parameter | Description | Default Value |
| Critical Step | Defines whether the step is critical for machine recovery.  If you mark the step as Critical, its failure for a machine from a critical inventory group will halt the plan. | Yes |
| Run Step During a DataLab Test | Defines whether the step will be executed during plan testing in a DataLab. | Yes |
| Run Step During Undo and Failback | Defines whether the step will be executed during the Failback and Undo Failover operations. | No |
| Timeout | Maximum amount of time (in seconds) for the step to execute. | 300 |
| Retries | Number of retries that will be attempted if the step fails on the first try. | 10 |
| Script Execution Location | Defines whether the script will run on the Veeam Backup & Replication server, on the Orchestrator server or on the in-guest OS. | In-Guest OS (not editable) |
| Windows Credentials | Credentials required to gain access to the SQL Server instance that uses Windows Authentication.  If the SQL Server instance you want to check uses Windows Authentication, the provided credentials will be used to connect to both the in-guest OS and the SQL instance. In this case, specify a value for the Windows Credentials parameter, and leave the [SQL Credentials](#sqlcreds) parameter value empty. | — |
| SQL Credentials | SQL account credentials required to gain access to the SQL Server instance that uses SQL Server Authentication.  If the SQL Server instance you want to check uses SQL Server Authentication, Orchestrator will use SQL Server credentials to access the SQL instance, and Windows credentials to access the in-guest OS. That is why you must specify values for both the SQL Credentials and [Windows Credentials](#wincreds) parameters.  Note: The SQL Credentials parameter does not accept Windows credentials. | — |
| SQL Instance | Name of the SQL instance to check.  Note: To check all detected instances, select ALL. | ALL |
| SQL Database | Name of the SQL database to check.  Note: To check all detected databases, select ALL. | ALL |


