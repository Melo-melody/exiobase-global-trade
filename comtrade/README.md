# UN Comtrade API Trade Data Analysis

## Overview
This project reports on **tariffs, product prices, and trade data** by country, enabling the assembly of a **basket of goods** using **Harmonized System (HS) codes**. It ensures integration-ready workflows for **Model.Earth** by providing **Jupyter Notebooks, processed datasets (CSV), and visualizations** (bar chart, line chart, heatmap) to analyze global trade trends.

## Objectives
- Fetch trade data related to **consumer products, prices, and tariff rates** by country.
- Report on **changing trade tariffs** and their impact.
- Assemble a **basket of goods** using industry sector or **Harmonized System (HS) codes**.
- Provide **reproducible** outputs for further analysis and integration.

## Implementation
### 1. Data Retrieval
- Used **Python** and **Jupyter Notebook** (`comtrade-report.ipynb`) to query the **UN Comtrade API**.
- Query parameters include:
  - **Reporter Country**: e.g., USA or any other country.
  - **Partner Country**: World or specific trade partners (e.g., China).
  - **Year**: Data retrieved from 2000 onwards.
  - **Product Classification**: HS codes or all available products.

### 2. Data Processing
- **Converted** the `period` column into **datetime format** for time-series analysis.
- **Filtered and cleaned** the dataset to remove unnecessary metadata.
- **Aggregated** total records by **reporter country, partner, and time period**.

### 3. Data Analysis & Visualization
- **Exploratory Data Analysis (EDA)** performed on **past one-year** data:
  - **Trade volume trends** over time.
  - **Top trading countries** ranked by total records.
  - **Trade flow heatmaps** to analyze country-level variations.

#### Generated Visualizations:
- 📊 **Bar Chart**: Top 10 countries by total trade records.
- 📈 **Line Chart**: Trade volume trends over the past year.
- 🔥 **Heatmap**: Trade relationships across different time periods.

## Next Steps
- 🛠 **Feedback Integration**: Refine visualizations based on Model.Earth team input.
- 📊 **Advanced Analysis**: Include product-specific trade patterns if required.
- ☁ **Deployment**: Prepare scripts and notebooks for cloud-based API integration.

## Conclusion
- **UN Comtrade API** provides robust trade and tariff data for analysis.
- The processed dataset and visualizations enable **data-driven insights** into global trade.
- The solution is **scalable, reproducible, and ready** for further integration.

## Files & Attachments
- 📂 **`comtrade-report.ipynb`**: Jupyter Notebook with API queries and data processing.
- 📄 **`comtrade-output.csv`**: Cleaned dataset for further analysis.
- 📜 **`comtrade-report.pdf`**: Documentation outlining the project scope and methodology.

---

### 🚀 Get Started
To reproduce the analysis, open `comtrade-report.ipynb` and follow the provided steps.

---


### Issue:

Unable to limit rows returned. Tried maxrec, count, max, and cdlimit parameters to limit the records. Instead, the API returns all available records.

[Example of API call](https://comtradeapi.un.org/public/v1/getDATariffline/C/M/HS?reporter=USA&year=2020&trade_type=1)
