# MSCDA Group 3 - SSIS ETL Project

Group SSIS (SQL Server Integration Services) project for the MSc Data Analytics coursework. It follows a parent/child ETL pattern that extracts data from the Northwind sample database, stages it, and loads the target warehouse. The default branch, `Upsert-Statement`, contains the current work on incremental (upsert) loads.

## Packages

| Package | Purpose |
|---------|---------|
| `Parent.Package.dtsx` | Orchestrates the run |
| `Package.dtsx` | Main load package |
| `Child.Extracting.dtsx` | Extracts data from the Northwind source |
| `Child.Staging.dtsx` | Stages extracted data before the final load |

Connection managers point at the local Northwind source and the SQL Express target; `Project.params` holds project-level parameters.

## Opening the project

1. Open `MSCDA_GROUP3.sln` in Visual Studio with the SSIS extension (SSDT).
2. Point the connection managers at your own Northwind source and target database.
3. Run `Parent.Package.dtsx`.
