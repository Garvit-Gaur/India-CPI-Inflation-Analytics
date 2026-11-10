# Original Workbook Guide

The original `.xlsb` workbook is preserved in `source/`.

| Sheet | Purpose |
|---|---|
| `Raw_Data` | Wide-form monthly CPI source data |
| `Clean Data` | Long-form analysis dataset with CPI index, MoM, and YoY fields |
| `Category_Mapping` | Category-to-broader-bucket lookup |
| `Q1_Contribution` | Existing workbook analysis output for category contribution |
| `Q2_YoY_Trend` | Existing workbook output for annual YoY trend |
| `Q3_Food_Inflation` | Existing workbook output for food inflation |
| `Q4_COVID_Impact` | Existing workbook output for pre/post-COVID comparison |
| `Q5_Oil_Correlation` | Existing workbook output for Fuel and light correlation |
| `Summary` | Narrative summary of the workbook's findings |

The notebook recomputes analysis from the clean data rather than relying on the pivot output tabs. See the notebook's methodology notes for scope and interpretation.
