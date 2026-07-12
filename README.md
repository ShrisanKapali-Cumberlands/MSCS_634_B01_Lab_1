# 📊 Iowa Liquor Sales 2025: Data Analysis & Preprocessing

**Student:** Shrisan kapali  
**Professor:** Satish Penmatsa  
**Course:** Advanced Big Data and Data Mining (MSCS 634 B01)  
**Date:** 07/12/2026

---

## 🎯 Purpose of the Project

This repository contains the completion of a Data Science Laboratory assignment focused on end-to-end data processing. The primary purpose of this project is to apply foundational and advanced data visualization, data preprocessing, and statistical analysis techniques to a real-world, large-scale administrative dataset.

By utilizing the **Iowa State Liquor Sales dataset (2025)**, this project transitions raw data into a clean, analytical format. The workflow facilitates a deeper analysis of retail trends by applying programmatic preprocessing techniques, specifically utilizing Interquartile Range (IQR) calculations to detect massive outliers, and employing a MinMax Scaler to normalize features for comparative statistical modeling.

## 🗄️ The Dataset

- **Source:** [Data.gov - Iowa Liquor Sales](https://catalog.data.gov/dataset/iowa-liquor-sales-2025?from_hint=eyJxIjoiaW93YSBsaXF1b3Igc2FsZXMifQ%3D%3D)
- **Size:** ~769,495 sales records
- **Description:** Real-world government administrative data tracking wholesale liquor purchases by retailers across the state of Iowa, including geographic, categorical, and financial metrics.
- **Important Note on Running the Project:** Due to GitHub's file size limits, the raw data is provided in a compressed file named `IOWA_Liquor_Sales.zip`. **Please extract this zip file to access the underlying `.csv` dataset before running the Jupyter Notebook.**

## 🛠️ Technologies Used

- **Environment:** Jupyter Notebook
- **Language:** Python 3
- **Libraries:**
  - `pandas` (Data manipulation, missing value handling, programmatic cleaning)
  - `numpy` (Numerical operations)
  - `matplotlib` & `seaborn` (Data visualization and correlation heatmaps)
  - `scikit-learn` (Data scaling via `MinMaxScaler`)

## 📈 Key Insights from Visualizations & Statistics

A comprehensive suite of visualizations and statistical measures was generated to explore the dataset, revealing several distinct market trends:

- **Bar Chart (Top 10 Bottles Sold by Category):**
  - **American Vodkas** overwhelmingly dominate the Iowa market in sheer volume, with nearly 2.0 million bottles sold.
  - They are followed by **Whiskey Liqueur** (~1.45M) and **Canadian Whiskies** (~900K).
  - Conversely, categories like Mixto Tequila and Cocktails/RTD sit at the bottom of the top 10, each hovering around 200,000 bottles sold.
- **Box Plot (Sales Distribution by Category):**
  - Despite moving the highest volume of bottles, American Vodkas have the **lowest median transaction value** and the narrowest distribution among the top 5 categories.
  - In contrast, **100% Agave Tequila** shows the highest median sales amount and the widest interquartile range, indicating strong premium pricing variance where individual transactions yield much higher revenue.
- **Scatter Plot (Sales Amount vs. Gallons Sold):**
  - While there is an expected positive correlation between volume and revenue, the vast majority of sales cluster tightly under 500 gallons and $50,000.
  - This plot successfully isolated a **massive outlier in American Schnapps**, detailing a single anomaly transaction of roughly 3,500 gallons exceeding $250,000 in sales.
- **Line Plot (Daily Sales Over Time):**
  - Temporal mapping uncovered a highly cyclical, repeating sales pattern.
  - Total daily sales consistently **peak between $1.5 million and $2.2 million** before dropping sharply to near zero on a regular interval, likely reflecting predictable weekly fulfillment cycles, closed store days, or reporting batch schedules.
- **Statistical Analysis & Correlation Matrix:**
  - The Pearson correlation heatmap revealed a moderate positive correlation (0.54) between `sales_dollars` and volume metrics (`sales_liters` / `sales_gallons`). This mathematically supports the box plot insight: volume isn't the sole driver of revenue, as category pricing heavily dictates final transaction dollars.
  - Additionally, the `pack` variable demonstrated a positive correlation (0.65) with `sales_bottles` but a negative correlation (-0.40) with `bottle_volume_ml`, confirming that spirits sold in higher pack quantities consistently feature smaller individual bottle volumes.

## 🚧 Challenges Faced and Decisions Made

Executing this end-to-end data pipeline presented several technical learning opportunities:

1. **Adapting to Jupyter Notebooks:** Transitioning to a cell-based execution environment involved a distinct learning curve. A significant hurdle was managing dataframe states, which required learning and implementing new commands like `.copy()` before data cleaning blocks to successfully preserve the raw data and avoid `SettingWithCopyWarning` errors.
2. **Iterative Visualization Design:** Generating clean, readable graphs required extensive troubleshooting of `matplotlib` and `seaborn` syntax. I had to experiment heavily with formatting the correct axes and placing legends properly. Furthermore, through trial and error, I realized the raw dataset contained too many unique items to visualize legibly; this led to the necessary decision of filtering the data down to the "Top 10" or "Top 5" categories so the charts could provide actual, readable insights.
3. **Locating Exact Commands:** Finding and applying precise programmatic commands—such as generating specific quantiles for IQR outlier detection, merging side-by-side comparative dataframes for data quality reporting, and setting up the `MinMaxScaler`—required significant problem-solving and documentation review.

## 📸 Documentation

A full suite of screenshots documenting the preprocessing steps, before-and-after data states, and analytical outputs are included in this repository.

**Data Exploration & Visualization:**

- `First_5_Row_Using_Head()`
- `Display_Info`
- `Scatter_Plot_Sales_Gallons_VS_Sales_Dollars`
- `Scatter_Plot_Sales_Gallons_VS_Sales_Dollars_with_Insight`
- `Bar_Chart_Top_10_Bottles_Category_Sold`
- `Bar_Chart_Top_10_Bottles_Category_Sold_With_Insights`
- `Box_Plot_Top_5_Sales_Categories`
- `Box_Plot_Top_5_Sales_Categories_With_Insights`
- `Line_Plot_Daily_Sales_Over_Time`
- `Line_Plot_Daily_Sales_Over_Time_With_Insights`

**Data Preprocessing:**

- `Handling_Missing_Data_Before_After`
- `IQR_Calculation_And_Stats`
- `IQR_Calculation_Missed_Categories`
- `Data_Reduction_Before_And_After_Shape`
- `Data_Scaling_Using_MinMax_Scaler`

**Statistical Analysis:**

- `DF_Scaled_Describe`
- `Central_Tendency_Min_max_median_mode`
- `Dispersion_Measures`
- `Correlation_Analysis_Table`
- `Correlation_Matrix_Heatmap`
