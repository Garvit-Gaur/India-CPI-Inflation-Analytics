# Data Dictionary

## cpi_raw_data.csv

Wide-form source table. One row per sector/month; columns contain CPI index values for individual categories and the General index.

| Field | Description |
|---|---|
| `Sector` | Rural, Urban, or Rural+Urban |
| `Year` | Calendar year |
| `Month` | Month name |
    | `Cereals and products` | CPI index for the named category/aggregate |
| `Meat and fish` | CPI index for the named category/aggregate |
| `Egg` | CPI index for the named category/aggregate |
| `Milk and products` | CPI index for the named category/aggregate |
| `Oils and fats` | CPI index for the named category/aggregate |
| `Fruits` | CPI index for the named category/aggregate |
| `Vegetables` | CPI index for the named category/aggregate |
| `Pulses and products` | CPI index for the named category/aggregate |
| `Sugar and Confectionery` | CPI index for the named category/aggregate |
| `Spices` | CPI index for the named category/aggregate |
| `Non-alcoholic beverages` | CPI index for the named category/aggregate |
| `Prepared meals, snacks, sweets etc.` | CPI index for the named category/aggregate |
| `Food and beverages` | CPI index for the named category/aggregate |
| `Pan, tobacco and intoxicants` | CPI index for the named category/aggregate |
| `Clothing` | CPI index for the named category/aggregate |
| `Footwear` | CPI index for the named category/aggregate |
| `Clothing and footwear` | CPI index for the named category/aggregate |
| `Housing` | CPI index for the named category/aggregate |
| `Fuel and light` | CPI index for the named category/aggregate |
| `Household goods and services` | CPI index for the named category/aggregate |
| `Health` | CPI index for the named category/aggregate |
| `Transport and communication` | CPI index for the named category/aggregate |
| `Recreation and amusement` | CPI index for the named category/aggregate |
| `Education` | CPI index for the named category/aggregate |
| `Personal care and effects` | CPI index for the named category/aggregate |
| `Miscellaneous` | CPI index for the named category/aggregate |
| `General index` | CPI index for the named category/aggregate |

## cpi_clean_data.csv

Long-form analysis table, one record per sector, month, and category.

| Field | Description |
|---|---|
| `Sector` | Rural, Urban, or Rural+Urban |
| `Year` | Calendar year |
| `Month` | Month name |
| `Month Number` | Numeric month (1–12) |
| `Date` | Excel serial date from source workbook |
| `Category` | CPI category or aggregate |
| `CPI_Index` | CPI index value |
| `Broader_Category` | Broader category mapping |
| `MoM_Inflation_%` | Month-on-month inflation percentage supplied in workbook |
| `YoY_Inflation_%` | Year-on-year inflation percentage supplied in workbook |

## category_mapping.csv

Maps each CPI `Category` to a `Broader_Bucket` used for grouped analysis.
