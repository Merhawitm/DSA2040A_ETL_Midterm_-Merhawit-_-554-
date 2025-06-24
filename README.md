# ETL Midterm Project – Merhawit (ID: 554)

##  Project Overview

This ETL (Extract, Transform, Load) midterm project demonstrates the process of building a simple but complete ETL pipeline using Python. It covers how raw CSV data is extracted, cleaned, transformed, and loaded into structured storage formats like SQLite databases. The project simulates a real-world data engineering workflow used in data analytics, machine learning, and business intelligence.

---

##  ETL Phases Breakdown

### 1. **Extraction (`etl_extract.ipynb`)**
- Loads `raw_data.csv` and `incremental_data.csv` from the `/data` directory.
- Displays the first 5 rows, data structure, missing values, and duplicates.
- Saves copies of the raw and incremental data for backup.

### 2. **Transformation (`etl_transform.ipynb`)**
- Cleans missing values, removes duplicates, and performs data type corrections.
- Adds derived columns like `total_price` and extracts the purchase day from date fields.
- Generates visualizations: missing values heatmaps, sales trends, customer behavior, etc.
- Saves cleaned datasets to the `/transformed` folder as:
  - `transformed_full.csv`
  - `transformed_incremental.csv`

### 3. **Loading (`etl_load.ipynb`)**
- Loads the transformed CSVs into SQLite databases using `sqlite3`.
- Stored in the `/loaded` folder as:
  - `full_data.db` with table `full_data`
  - `incremental_data.db` with table `incremental_data`
- Verifies the result using SQL queries (e.g., `SELECT * FROM full_data LIMIT 5`) and `.head()` calls.

---

##  Tools & Technologies Used

| Tool         | Purpose                              |
|--------------|---------------------------------------|
| **Python 3.x**     | Core programming language             |
| **Pandas**         | Data wrangling and transformations    |
| **Matplotlib**     | Plotting and visualization            |
| **Seaborn**        | Statistical data visualizations       |
| **SQLite3**        | Lightweight SQL database for loading  |
| **Jupyter Notebook** | Interactive ETL notebook development |
| **os**             | File and folder management            |
| **scikit-learn**   | Used for regression-based imputation  |

---

## ▶How to Run the Project

> Ensure you have Python, pandas, and Jupyter installed before starting.

### Step 1: Clone the Repo
```bash
git clone https://github.com/Merhawitm/DSA2040A_ETL_Midterm_-Merhawit-_-554-.git
cd DSA2040A_ETL_Midterm_-Merhawit-_-554-
Step 2: Open Notebooks
Launch Jupyter and open the notebooks in this order:

etl_extract.ipynb – View raw data and save backups

etl_transform.ipynb – Clean, enrich, and visualize the data

etl_load.ipynb – Save data to SQLite and preview with queries
# 3 Project Structure
ETL_Midterm_Merhawit_554/
├── data/
│   ├── raw_data.csv
│   └── incremental_data.csv
├── transformed/
│   ├── transformed_full.csv
│   └── transformed_incremental.csv
├── loaded/
│   ├── full_data.db
│   └── incremental_data.db
├── etl_extract.ipynb
├── etl_transform.ipynb
├── etl_load.ipynb
├── screenshots/
│   ├── data_preview.png
│   └── customer_spending.png
├── README.md
└── .gitignore
# 5. Sample Output / Screensho
# Plot spending distribution
! [image](https://github.com/user-attachments/assets/b7ab945e-c238-4e30-95ea-dd701dc0fa44)

Sales by Day of Week (Transformed Data)
! [image](https://github.com/user-attachments/assets/fc16f1d0-5266-4cd0-bbca-d7ee58ca68b2)




