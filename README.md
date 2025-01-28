# Revenue Cycle Management: End-to-End Data Engineering Pipeline on Azure
This is an end-to-end data engineering pipeline designed for Revenue Cycle Management (RCM). The pipeline enables trendy hospital to efficiently monitor their financial aspects, including patient scheduling, claims processing, and provider payments, by processing and transforming electronic hospital records, provider details, and insurance-related data.

## Project Overview

To provide a streamlined approach for integrating and analyzing data from various sources to support the financial operations of trendy hospitals.

### Data Sources
- Electronic Medical Records (EMR) from all hospital branches.
    - Patient
    - Department
    - Transaction
    - Encounter
    - Provider
- Claims Data from insurance providers for all hospital branches.
- API Extract:
   - National Provider Identity (NPI)
   - International Classification of Diseases (ICD) codes
- Current Procdeural Terminology (CPT) codes
  
## Pipeline Architecture
Initial Pipeline: Copy activity to load EMR data from landing into prepared hospital database

View Project Architecture [here](https://github.com/Choiceugwuede/Hospital-Revenue-Cycle-Management-Pipeline/blob/main/Pipeline%20Architecture.png)

The main pipeline processes data through three main stages:
1. Bronze Layer:
   - Dynamic Raw data ingestion from all source in parquet format
   - Source of Truth
2. Silver Layer:
   - Purpose: Transformation and enrichment of the data in delta format
   - Operations:
      - Data Validation Checks
      - Deduplication
      - Applying business rules
      - Merge for Incremental datasets (when matched/ not matched)
      - Common Data Model (CDM)
      - SCD2 Implementation
3. Gold Layer:
   - Purpose: Final dataset for analysis and reporting.
   - Operations:
      - Filtering for quality (e.g., is_current = true, is_quarantined = false)
      - Aggregations for key metrics
      - Fact and Dimension Tables Creation

## Tools and Technologies
 - Azure Data Lake Storage: Containers for landing, bronze, silver, and gold
 - Azure Data Factory (ADF): Orchestration of data pipelines.
 - Delta Lake: Storing bronze, silver, and gold data.
 - Databricks: For transformations, SQL queries, and Delta Lake management.

## Key Outcome
Centralized data repository for Revenue Cycle Management.

   





