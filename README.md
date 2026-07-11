# 📊 Iowa Liquor Sales 2025: Data Analysis & Preprocessing

**Student:** Shrisan kapali  
**Professor:** Satish Penmatsa  
**Course:** Advanced Big Data and Daa Mining (MSCS 634 B01)  
**Date:** 07/12/2026

---

## 🎯 Purpose of the Project

This repository contains the completion of a Data Science Laboratory assignment focused on end-to-end data processing. The primary purpose of this project is to apply foundational and advanced data visualization, data preprocessing, and statistical analysis techniques to a real-world, large-scale administrative dataset.

By utilizing the **Iowa State Liquor Sales dataset (2025)**, this project transitions raw data into a clean, analytical format. The workflow facilitates a deeper analysis of retail trends by applying programmatic preprocessing techniques, specifically utilizing Interquartile Range (IQR) calculations to detect massive outliers, and employing a MinMax Scaler to normalize features for comparative statistical modeling.

## 🗄️ The Dataset

- **Source:** [Data.gov - Iowa Liquor Sales](https://catalog.data.gov/dataset/iowa-liquor-sales-2025?from_hint=eyJxIjoiaW93YSBsaXF1b3Igc2FsZXMifQ%3D%3D)
- **Size:** ~769,495 sales records
- **Description:** Real-world government administrative data tracking wholesale liquor purchases by retailers across the state of Iowa, including geographic, categorical, and financial metrics.

## 🛠️ Technologies Used

- **Environment:** Jupyter Notebook
- **Language:** Python 3
- **Libraries:**
  - `pandas` (Data manipulation, missing value handling, programmatic cleaning)
  - `numpy` (Numerical operations)
  - `matplotlib` & `seaborn` (Data visualization and correlation heatmaps)
  - `scikit-learn` (Data scaling via `MinMaxScaler`)

## 📈 Key Insights from Visualizations & Statistics

A comprehensive suite of visualizations and statistical measures was generated to explore the dataset:

- **Scatter Plot (Sales Amount vs. Gallons Sold):** Visualizing these continuous variables revealed a strong positive correlation. The spread of data points highlighted distinct price tiers, illustrating the difference between high-volume budget sales and low-volume premium spirits.
- **Box Plot (Sales Distribution by Category):** This plot successfully visualized data spread and isolated transaction skewness. It demonstrated how specific categories experience much wider variances in transaction sizes than others.
- **Bar Chart (Top 10 Bottles Sold by Category):** Highlighted the most dominant spirit categories in the Iowa market, showing which types of liquor drive the highest consumer demand and state revenue.
- **Line Plot (Daily Sales Over Time):** Mapping total sales chronologically uncovered distinct temporal purchasing cycles, including peaks corresponding to weekend/holiday stocking and valleys representing low-activity days.
- **Statistical Analysis:** Central tendency and dispersion measures provided concrete numerical boundaries for the data. The subsequent Pearson correlation matrix quantified the exact linear relationships between variables like sales dollars, liquid volume, and bottles sold.

## 🚧 Challenges Faced and Decisions Made

Executing this end-to-end data pipeline presented several technical learning opportunities:

1. **Jupyter Notebook Environment:** Adapting to the cell-based execution style required a learning curve, particularly regarding state management. A key decision was instituting the best practice of utilizing `.copy()` at the start of data cleaning blocks to ensure raw dataframes were preserved without throwing `SettingWithCopyWarning` errors.
2. **Creating Visualizations:** Constructing the plots required troubleshooting `matplotlib` and `seaborn` syntax. Decisions had to be made regarding formatting, scaling axes, and ensuring legends and labels displayed cleanly for presentation.
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
