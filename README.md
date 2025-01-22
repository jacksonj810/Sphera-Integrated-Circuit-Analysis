# Sphera-Integrated-Circuit-Analysis

## Overview
This project analyzes a dataset of Sphera Integrated Circuits (ICs) with the goal of uncovering relationships between factors such as cost, power dissipation, process node, lead count, and package type. By utilizing Python in a Jupyter Notebook, the project cleans and explores the data, then visualizes key findings using matplotlib and seaborn. The results can improve sourcing decisions, highlight potential cost drivers, and inform package/family selections.

## Key Features
- Data Cleaning & Preparation:
  - Handled missing values, standardized columns (e.g., removing “mm”, “nm”), and ensured correct data types were used for each respective column.
- Data Analysis:
  - Correlation matrix to identify links between lead count, node size, power dissipation, and cost.
  - Histograms to show distribution of Max Power Dissipation and Average Cost, showing potential outliers and skewed distributions.
- Comparisons & Groupby:
  - Grouped by Package Type to see how it relates to max power dissipation.
  - Examined how distributor pricing (DigiKey, Arrow, Mouser, Rochester, Avnet) varies for similar parts.
- Visualizations:
  - Scatter plots to illustrate relationships (e.g., Power vs. Cost, Node size vs. Cost).
  - Bar charts and histograms to highlight distributions, outliers, and relative differences.

## Folder Structure
- **Code/**: Jupyter notebooks for data cleaning and analysis.
- **Data/**: Datasets used for analysis
- **Results/**: Detailed report, graphs

## Analysis Highlights
- **Correlation Matrix**:
  - Showed lead count has a strong positive correlation with cost, suggesting higher-pin devices are generally pricier.
  - Weak correlation between power dissipation and cost, indicating other factors might drive pricing more.
- **Scatter Plots**:
  - Power Dissipation vs. Cost: Slight positive slope but no strong linear pattern.
  - Node vs. Cost: Mild negative slope, hinting smaller node processes could cost more, though not conclusively.
- **Mean Max Power Dissipation by Package Type**:
  - Certain packages (e.g., QFN, SSOP, DIP, BGA) handle higher wattage, while others (TSSOP, TSOP) align with lower wattage parts.
- **Distributions of Power & Cost**:
  - Both exhibit right-skewed shapes, indicating a handful of high-power or high-cost outliers.
- **Distributor Price Summary**:
  - Highlights variance in mean/median prices per distributor.
  - Reveals which sellers potentially offer lower or higher-cost deals, though availability differs.

## Tools Used
- Python (Pandas, NumPy, matplotlib, seaborn)
- Jupyter Notebook

## Next Steps
- Multivariate Regression: Incorporate lead count, node, family, and package type to better predict cost.
- Expand Dataset: Include more factors (e.g., clock speed, memory size) or more IC families to improve analysis.
- Interactive Reporting: Potentially build a simple web-based dashboard for better filtering and exploration.

## Data Source
This project’s IC data was assembled from Sphera notes, distributor websites, and datasheets. Fields include cost at different quantities (from major distributors), in addition to power dissipation, packaging, and node sizes from datasheets.
