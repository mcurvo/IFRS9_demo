# IFRS9

Just a quick weekend project to understand how to calculate and stress-test Expected Credit Loss (ECL) under IFRS 9 using Python

## What’s inside

* **data/**: CSV files with historical macroeconomic data (`HistoricalMEV.csv`), forecast scenarios (`ForecastedMEV.csv`), and sample customer information.
* **01\_load\_clean\_\_eda\_model\_staging.ipynb**:

  * **Data loading:** Read in historical and forecast CSVs along with customer and limit data.
  * **Cleaning:** Identify and handle missing values.
  * **Basic EDA:** Plot distributions and correlations to spot trends (e.g., GDP vs. default rates).
  * **Model staging :** Set up a simple ECL prediction.
* **02\_scenario\_analysis\_and\_stress\_testing.ipynb**:

  * **Load results:** Import precomputed ECL outputs from the first notebook.
  * **Scenario comparison:** Calculate average macro variables for Base, Best, and Worst cases.
  * **Adjustment factors:** Derive factors by comparing scenario means to the base case.
  * **Stress testing:** Apply these factors to ECL values to simulate stressed allowances.
  * **Summary:** Generate tables (and optional charts) showing the impact of each scenario.
* **requirements.txt**: List of Python libraries needed (pandas, numpy, scikit-learn, matplotlib, xgboost, LightGBM, etc.).
