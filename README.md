# Noodles Crypto Analytics Platform

## Project overview
An analytics project combining Python data preparation, a MySQL data warehouse, aggregation views, and interactive Power BI reports for currency and social-engagement analysis.

## Architecture
JSON files → Python/pandas → MySQL `noodles_dw` → aggregation tables/views → Power BI.
See [architecture diagram](docs/architecture-diagram.png).

## Technology stack
Python, pandas, SQLAlchemy, MySQL, Jupyter notebooks, Power BI Desktop and DAX.

## Data model
Documented core objects include `DimCurrency`, `DimDate`, `DimPlatform` and `FactSocialEngagement`. Verify exact fields and counts against the local database.

## Reports
- Task 7: `reports/NoodlesCrypto_TopPerformers.pbix`
- Task 8: `reports/NoodlesCrypto_ExecutiveDashboard.pbix`

## Documentation
- [Data dictionary](docs/data-dictionary.xlsx)
- [Technical runbook](docs/technical-runbook.md)
- [User guide](docs/user-guide.md)
- [Final checklist](docs/final-checklist.md)
- [Demo presentation](docs/demo-presentation.pptx)

## Refreshing
Follow `docs/technical-runbook.md`. Add actual connection details, refresh duration, and schedule only after verifying them. Never commit secrets.

## Demo
Watch the 10-minute project demonstration: Noodles Crypto Analytics – Demo Video
