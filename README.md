# 📊 Power BI Power Query Data Transformation Project

An end-to-end data preparation and ETL (Extract, Transform, Load) project demonstrating advanced data cleaning, shaping, and modeling techniques in Power BI. This project transforms raw, inconsistent transaction logs into a clean, analysis-ready star schema.

### 🎯 Project Objectives

- Clean and standardize merchant metadata.
- Build a comprehensive date dimension for temporal analysis.
- Normalize and reshape category structures using Unpivot.
- Filter and discard low-value noise to target meaningful financial activity.
- Consolidate multi-year transaction datasets via Append Queries.
- Integrate fact and dimension tables using Merge Queries.
- Establish business-driven categorization rules with Conditional Columns.
- Perform high-level merchant aggregation and transaction value analysis.



### 📂 Datasets Used
- **fact_transactions_2022**: Raw ledger entries for the year 2022.
- **fact_transactions_2023**: Raw ledger entries for the year 2023.
- **dim_merchants**: Merchant details containing raw text strings and industry classifications.
- **pivoted_dim_category**: Category attributes structured in a pivoted format
- **dim_date**: Calendar lookup table.

###   🛠️ Step-by-Step ETL & Power Query Workflow
**Task 1**: Merchant Data Cleaning (dim_merchants)
- **Split Column**: Separated merchant titles using the delimiter  - .
- **Industry Segment**: Extracted industry segments from text strings enclosed in parentheses ( ).
- **Text Hygiene**: Applied Trim to eliminate leading and trailing whitespace.
- **Deduplication**: Removed redundant merchant records while preserving unique IDs.
