# NYC Taxi Data Engineering & Analytics Pipeline

An end-to-end data engineering and analytics project built using **Python, PySpark, SQL, Azure Databricks, Delta Lake, and Power BI**. This project processes NYC taxi trip data through a Medallion Architecture (Bronze, Silver, and Gold) and presents business insights through an interactive Power BI dashboard.

## Project Overview

The goal of this project is to build a data pipeline that ingests, transforms, validates, and analyzes NYC taxi trip data.

The pipeline follows the **Medallion Architecture**:

- **Bronze Layer:** Ingests raw NYC taxi CSV data into Delta tables.
- **Silver Layer:** Cleans and transforms data using PySpark and SQL.
- **Gold Layer:** Creates aggregated datasets for business analysis and reporting.

The processed data is connected to Power BI to create an interactive analytics dashboard.

## Architecture

```text
NYC Taxi CSV Dataset
        |
        v
  Bronze Layer
  (Raw Data Ingestion)
        |
        v
  Silver Layer
  (Data Cleaning & Transformation)
        |
        v
   Gold Layer
  (Business Aggregations)
        |
        v
  Power BI Dashboard
  (Data Visualization)
```

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data processing and scripting |
| PySpark | Data transformation |
| SQL | Data analysis and validation |
| Azure Databricks | Data engineering platform |
| Delta Lake | Storage and data management |
| Databricks Jobs | Pipeline task orchestration |
| Auto Loader | File-ingestion functionality testing |
| Power BI | Interactive dashboards and visualization |
| Git & GitHub | Version control and project hosting |

## Project Workflow

### 1. Bronze Layer – Data Ingestion
- Ingested NYC taxi trip data from a CSV dataset into Databricks.
- Stored raw data in Delta format.
- Performed initial record-count and data-quality checks.
- Added ingestion-related metadata where applicable.

### 2. Silver Layer – Data Transformation
- Cleaned and transformed raw data using PySpark and SQL.
- Performed data validation checks.
- Checked for null values and duplicate records.
- Created a structured dataset for downstream analysis.

### 3. Gold Layer – Business Aggregations
Created analytical datasets to understand taxi trip patterns:

- **Vendor Analysis:** Total trips and average, minimum, and maximum trip duration by vendor.
- **Passenger Analysis:** Trip distribution by passenger count.
- **Hourly Analysis:** Taxi demand across different hours.
- **Daily Analysis:** Daily trip trends.

### 4. Pipeline Automation
- Configured a multi-task Databricks Job.
- Organized ingestion, transformation, Gold-layer processing, and data-quality tasks.
- Configured a daily schedule and successfully tested a job run.

### 5. Data Quality & Incremental Load Testing
- Validated record counts and checked for duplicate and null IDs.
- Implemented batch-based incremental ingestion logic.
- Tested duplicate-batch handling.
- Experimented with Auto Loader using an isolated test dataset and checkpoint location.

### 6. Power BI Dashboard
Connected Gold-layer Delta tables to Power BI and developed an interactive dashboard containing:

- Total Trips
- Average Trip Duration
- Total Vendors
- Trips by Vendor
- Trips by Passenger Count
- Hourly Taxi Demand
- Daily Taxi Trip Trends

## Dashboard Preview

Added the dashboard screenshot inside the `screenshots` folder and name it:

`dashboard.png`

Then this preview will display in README.

## Repository Structure

```text
nyc-taxi-data-engineering-pipeline/
│
├── notebooks/
│   ├── 01_Bronze_Ingestion
│   ├── 02_Silver_Transformation
│   ├── 03_Gold_Transformation
│   ├── 04_Data_Quality
│   ├── 05_Incremental_Load
│   └── 06_Auto_Loader_Test
│
│
├── screenshots/
│   └── dashboard.png
│
└── README.md
```

## Key Learnings

- Building an end-to-end data pipeline using Databricks.
- Working with PySpark and SQL for data transformation.
- Implementing Bronze, Silver, and Gold layers.
- Using Delta Lake for structured data storage.
- Performing data validation and quality checks.
- Working with incremental batch processing and Auto Loader testing.
- Orchestrating pipeline tasks using Databricks Jobs.
- Connecting Databricks data to Power BI for reporting.

## Future Enhancements

- Integrate a fully automated file-arrival-based ingestion workflow.
- Improve pipeline monitoring and error handling.
- Add more business metrics and dashboard insights.
- Enhance incremental processing for newly arriving source files.

## Dataset

The project uses an NYC taxi trip dataset obtained from Kaggle.

The raw dataset is not included in this repository.

## Author

**Vikrant Pal**

Aspiring Data Engineer

**Skills:** Python | SQL | PySpark | Azure Databricks | Delta Lake | Power BI

---

If you find this project useful, feel free to explore the repository and share your feedback.
