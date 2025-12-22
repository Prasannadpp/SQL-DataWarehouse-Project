# SQL Data Warehouse Project

## Overview
This project implements a modern **SQL-based Data Warehouse** using the
**Medallion Architecture (Bronze, Silver, Gold)** with a strong focus on
**data quality, validation, and analytical readiness**.

## Architecture
- **Bronze Layer**: Raw data ingestion (no transformations)
- **Silver Layer**: Cleansed and validated data
- **Gold Layer**: Business-ready analytical datasets

## Project Structure
- `docs/` – Architecture and layer-level documentation
- `scripts/` – SQL transformations and ETL logic
- `tests/` – Data quality and validation checks
- `datasets/` – Source and sample datasets
- `report/` – Analysis and reporting artifacts

## How to Use
1. Review architecture details in `docs/`
2. Execute SQL scripts from `scripts/`
3. Run validation queries from `tests/`

## Notes
- Environment variables are managed via `.env` (see `.env.example`)
- This project is designed for incremental enhancement and learning

