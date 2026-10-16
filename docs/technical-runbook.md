# Technical Runbook: Noodles Crypto Analytics

## System overview
The documented workflow is JSON source files → Python/pandas preparation → MySQL `noodles_dw` star schema → aggregation tables/views → Power BI reports. Task 5–6 workflows are managed through Jupyter notebooks, including `05_data_warehouse_design.ipynb` and `06_powerbi_prep.ipynb` per the task brief.

## Refresh procedure
1. Confirm MySQL is running and `noodles_dw` is available.
2. Confirm the configured source JSON files exist and are readable.
3. Open the relevant notebook and run cells in order.
4. Run the validation/QA cells and review exceptions, row counts, and referential-integrity checks.
5. Open the required PBIX in Power BI Desktop and choose **Home → Refresh**.
6. Confirm all pages render; test slicers, cross-filtering, bookmarks, drill-through and tooltips.
7. Save the PBIX after a successful refresh.

## Success indicators
- Notebook completes without errors.
- Expected tables/views exist.
- Row counts match actual validation output.
- No unexpected orphan records or missing required keys.
- Power BI visuals render without source errors.

## Troubleshooting
**Python import error:** activate the intended environment and install only the packages required by the notebooks (the task brief mentions pandas, SQLAlchemy, PyMySQL, python-dotenv, matplotlib and seaborn).

**MySQL connection failure:** check service status, host, port, database name and credentials in local configuration. Never commit passwords or tokens.

**Empty tables:** verify source files, database/schema selection, notebook output and reject files; compare row counts across stages.

**Power BI refresh failure:** verify the MySQL/ODBC connection and credentials. If using Power BI Service, separately test gateway and dataset credentials.

## Scheduling and backups
The task brief provides example cron/Task Scheduler setups, but do not claim scheduling is active until tested. Record the actual schedule and refresh history. Back up MySQL using a method supported by the installed MySQL version; do not use SQL Server backup syntax for MySQL.

## Local details to fill in
- MySQL host/port: ____________________
- Refresh owner: ____________________
- Measured refresh duration: ____________________
- Last successful validation date: ____________________
