# Rainfall, Rice Production, and Rice Price Analysis — East Java (2022–2024)

This repository contains data wrangling, exploratory analysis, and visualizations relating rainfall, rice production, and rice prices in East Java for the period 2022–2024.

## Why this project

Understanding how rainfall patterns affect rice production and prices helps policy-makers and farmers to plan for climate variability and market shocks. This project brings together heterogeneous data sources (NetCDF, PDF, Excel), cleans and integrates them, and provides reproducible notebooks for analysis and visualization.

## Contents

- `data/raw/`        : original (unchanged) datasets
- `data/processed/`  : cleaned and integrated datasets ready for analysis
- `notebooks/`       : Jupyter notebooks for data wrangling and exploratory analysis
- `docs/`            : supporting documents, figures, and supplementary outputs

## Key insights (summary)

- Provincial-level correlations between rainfall and production are generally weak, likely due to spatial heterogeneity within the province.
- District-level relationships vary substantially; localized analyses reveal stronger rainfall–production associations in some districts.
- Rice prices remained elevated through 2024 despite partial rainfall recovery, suggesting other drivers (market factors, supply chains) are important.

## Data sources

- Rainfall: gridded climate datasets (NetCDF). See `data/raw/rainfall/` for original NetCDF files and metadata.
- Rice production: BPS annual reports (PDF). Source files are in `data/raw/production/`. PDF tables were extracted and cleaned.
- Rice prices: PIHPS Excel datasets. Raw files in `data/raw/prices/`.

If you plan to re-run the pipeline, check `data/raw/` for raw filenames and the notebooks that reference them.

## Reproducibility & running the analysis

1. Create a Python environment (recommended: conda)

   - Python 3.9+ recommended
   - Install dependencies: `pip install -r requirements.txt` (or `conda env create -f environment.yml` if provided)

2. Required libraries (representative)

   - pandas, numpy
   - xarray (for NetCDF handling)
   - tabula-py (PDF table extraction)
   - openpyxl (Excel reading)
   - matplotlib, seaborn

3. Notebooks (run in order)

   - `notebooks/01-data-wrangle.ipynb`  — raw data extraction and cleaning
   - `notebooks/02-integration.ipynb`    — joining datasets and creating analysis-ready tables
   - `notebooks/03-exploration.ipynb`    — exploratory analysis and visualizations

You can convert notebooks to scripts with `nbconvert` for non-interactive runs.

## Project structure (detailed)

- `data/raw/`        - Raw inputs (do not edit directly)
  - `rainfall/`      - NetCDF files and README describing variables
  - `production/`    - BPS PDFs and any intermediate CSV extracts
  - `prices/`        - PIHPS Excel files

- `data/processed/`  - Cleaned and merged datasets used by notebooks

- `notebooks/`       - Analysis notebooks (.ipynb) with narrative and plots

- `docs/`            - Static figures, additional notes, and reproducible outputs

## How to contribute

- Open an issue describing the proposed change or bug.
- For code/data changes, create a branch named `fix/...` or `feat/...`, add tests or an illustrative notebook, and open a pull request.
- Document any new data sources, transformations, and assumptions in the notebooks and update this README when needed.

## Authors

- Mohammad Tyas Subianto
- Aryanti Indah Lestari

## License

Add a `LICENSE.md` (e.g., MIT, CC-BY) if you intend to make the repository open-source. If unsure, discuss via an issue.

## Contact

For questions or collaboration, please open an issue or contact the authors listed above.
