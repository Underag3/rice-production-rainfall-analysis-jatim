# Rainfall, Rice Production, and Rice Price Analysis
## East Java (2022–2024)

Data wrangling and exploratory analysis of rainfall, rice production, and rice prices in East Java (2022–2024).

Project Overview:
This project focuses on data wrangling and exploratory data analysis of rainfall, rice production, and rice prices in East Java. Multiple heterogeneous data sources (NetCDF, PDF, and Excel) were cleaned, transformed, and integrated to examine temporal and spatial relationships.

Data Sources:
- Rainfall data: climate data in NetCDF format
- Rice production data: BPS annual PDF reports
- Rice price data: PIHPS Excel datasets

Tools & Libraries:
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- xarray
- tabula-py

Workflow:
1. Collect raw data from multiple heterogeneous sources
2. Clean and transform each dataset independently
3. Perform data quality checks
4. Integrate datasets using time-based keys
5. Conduct exploratory data analysis and visualization

Key Insight:
- Provincial-level correlations are weak due to spatial heterogeneity
- Significant variation exists across districts in rainfall–production relationships
- Rice prices remain elevated despite rainfall recovery in 2024

Repository Structure:
data/raw/        : original datasets
data/processed/  : cleaned and integrated datasets
notebooks/       : data wrangling and analysis notebooks
docs/            : supporting documents and figures

Author:
Mohammad Tyas Subianto,
Aryanti Indah Lestari
