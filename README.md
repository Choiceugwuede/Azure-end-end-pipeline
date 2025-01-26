# Revenue Cycle Management: End-to-End Data Engineering Pipeline on Azure
This is an end-to-end data engineering pipeline designed for Revenue Cycle Management (RCM). The pipeline enables trendy hospital to efficiently monitor their financial aspects, including patient scheduling, claims processing, and provider payments, by processing and transforming electronic hospital records, provider details, and insurance-related data.

## Project Overview
### Purpose

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
   - Current Procedural Terminology (CPT) codes

## Pipeline Architecture
Initial Pipeline: To load EMR data into prepared hospital database
The pipeline processes data through three main stages:



