# Data setup

This repository does not redistribute the source datasets. Download these files from their respective sources and save them locally in this directory before running the notebook:

| Local filename | Source | Expected format |
|---|---|---|
| `Superstore.csv` | [Superstore Dataset Final, Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) | CSV with 9,994 transaction lines and 21 original fields; date fields in U.S. month/day/year format |
| `Census.xlsx` | [U.S. Census Bureau: Monthly Retail Trade Survey data](https://www.census.gov/retail/data.html) | Excel workbook with year-named sheets `2014` through `2017`, two sections (**NOT ADJUSTED** and **ADJUSTED**), business labels in column B and months January–December in columns C–N |

The notebook accesses `data/Superstore.csv` and `data/Census.xlsx` **relative to the repository root**.

## Important reproducibility note

This analysis uses the **NOT ADJUSTED** Census rows for:

- `Retail and food services sales, total`
- `Furniture, home furn, electronics, and appliance stores`

The source workbook uploaded during project preparation contains historical worksheets, including 2014–2017. Its extracted January 2014 benchmark values are **376,896** (total retail) and **14,847** (furniture/electronics), in the workbook's stated units. Updated Census downloads may use different revisions or layouts and may not exactly reproduce those values. If your download differs, obtain the corresponding historical-format file or adapt the extraction code explicitly; do not silently treat changed data as identical.

**Publication policy:** Do not commit downloaded source data into this repository without checking the provider's reuse terms and whether the contents contain personal or sensitive information. `.gitignore` excludes datasets from version control.
