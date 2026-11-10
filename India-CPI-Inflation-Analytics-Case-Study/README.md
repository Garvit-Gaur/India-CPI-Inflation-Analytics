# India CPI Inflation Analytics Case Study

**Author:** Garvit Gaur

## Overview
An exploratory data analytics project using India's Consumer Price Index (CPI) data. It studies category-level CPI movement across Rural, Urban, and Rural+Urban sectors, with focused analysis of inflation trends, food-price volatility, the COVID-19 period, and correlations with the Fuel and light CPI series.

## Dataset
Source: the user-provided `CPI_Index CaseStudy(2).xlsb` workbook.

- **Raw_Data:** 372 rows × 30 columns (wide monthly sector-level data)
- **Clean Data:** 10,044 rows × 10 analysis columns (long-format category data)
- **Category_Mapping:** 27 category-to-broader-bucket mappings
- **Coverage:** January 2013 to May 2023
- **Sectors:** Rural, Urban, Rural+Urban
- **Categories:** 27

The original workbook is retained under `source/`. Analysis-ready CSV exports are in `data/`.

## Verified Findings
Recomputed from the supplied `Clean Data` table in the notebook:

- **Highest annual average General Index YoY inflation in 2017–2023:** 2022 at 6.62%
- **2020 annual average General Index YoY inflation:** 6.34%
- **Most volatile food categories by monthly inflation range (Jun 2022–May 2023):** Vegetables (16.90 percentage points) and Egg (16.07 percentage points)
- **Highest positive pre/post-COVID change in average YoY inflation:** Oils and fats (20.05 percentage points)
- **Highest correlation with Fuel and light CPI (Jan 2021–Apr 2023):** General index (r = 0.987)

These are descriptive results using the specified windows and calculations in the notebook. Correlation does not imply causation.

## Analysis Questions
1. Category coverage and CPI index profile
2. Year-on-year inflation trend (General Index, Rural+Urban)
3. Food inflation volatility (June 2022–May 2023)
4. Pre-COVID vs post-COVID inflation comparison
5. Relationship between Fuel and light CPI and other categories (January 2021–April 2023)

## Repository Structure
```text
India-CPI-Inflation-Analytics-Case-Study/
├── data/
│   ├── cpi_raw_data.csv
│   ├── cpi_clean_data.csv
│   └── category_mapping.csv
├── notebooks/
│   └── India_CPI_Inflation_Analysis.ipynb
├── source/
│   └── CPI_Index_CaseStudy_original.xlsb
├── visualizations/
├── README.md
├── DATA_DICTIONARY.md
├── WORKBOOK_GUIDE.md
├── requirements.txt
└── .gitignore
```

## Run the Project
```bash
pip install -r requirements.txt
jupyter notebook notebooks/India_CPI_Inflation_Analysis.ipynb
```
The notebook loads the CSV files from `data/`.

## Important Methodology Notes
- The workbook's CPI data ends in May 2023; it is not current CPI data.
- The notebook uses the supplied `MoM_Inflation_%` and `YoY_Inflation_%` columns rather than inferring inflation from index levels.
- The `Fuel and light` CPI index is used as a proxy series in the correlation analysis. The workbook does not provide a separate crude-oil price series, so this should not be described as a direct crude-oil correlation.
- CPI expenditure weights are not included in the structured dataset. Category counts or equal-category summaries are not official CPI contribution weights.
- Pearson correlation is descriptive and does not demonstrate causality.
