# Bicycle Sales Cohort & RFM Analysis

## Project Overview
This project involves a comprehensive analysis of transaction, customer demographic, and customer address data for a cycling accessories organization. The primary goal is to understand customer behavior, identify key retention patterns, and segment customers based on value.

## Data Cleaning & Preparation
Before analysis, the dataset underwent rigorous cleaning:
* **Imputation:** Missing gender values were imputed using a gender-guessing library based on first names. Outlier ages (e.g., 125 years old) were replaced with the median age of relevant job industry categories.
* **Standardization:** Handled inconsistent column headers and converted data types for numerical/date columns.

## Key Findings

### 1. Cohort Analysis (Retention)
Customers were grouped into cohorts based on their first transaction month to calculate monthly retention rates.
* **Observation:** Significant fluctuations in retention were observed, prompting deep-dives into specific months.

**Deep Dive: July 2024 Drop (Index 2 vs. 3)**
* **Demographics:** Marked decrease in female customers, specifically in Retail and Manufacturing.
* **Products:** Drop in purchases of Solex and Trek Bicycles.
* **Wealth:** Drop in 'Mass' and 'Affluent' customer segments.

**Deep Dive: October 2024 Spike (Index 2 vs. 3)**
* **Demographics:** Rise in senior customers (50-75) and a more diverse gender/geographic mix (NSW & QLD).
* **Products:** Increased sales for Mountain/Road lines and WeareA2B brand. Giant Bicycles remained stable.

### 2. RFM Segmentation
An RFM (Recency, Frequency, Monetary) model was built to segment customers into 'High', 'Medium', and 'Low' value categories.
* **Score Distribution:** Scores ranged from 33.8 to 3483.6 (Mean: 1747.5).

**Root Cause Analysis of High-Value Customers:**
* **Job Industry:** Manufacturing, Financial Services, and Health industries are top contributors to the high-value segment.
* **Profit Drivers:** Affluent female customers in VIC and affluent male customers in QLD generated the highest profit.
* **Low Performers:** Male customers with high net worth tended to contribute the *lowest* profit in the low-value group, suggesting a potential engagement gap.

## Exploratory Data Analysis (EDA) Highlights
* **Univariate & Multivariate Analysis:** Explored distributions of `list_price`, `standard_cost`, and `profit`.
* **Demographics:** Analyzed relationships between `wealth_segment`, `owns_car`, `job_industry_category`, and purchasing behavior.
* **Geographic:** Mapped state-wise distribution and property valuation patterns.

## Technologies Used
* **Python** (Pandas, NumPy)
* **Visualization** (Matplotlib, Seaborn)
* **Techniques** (Cohort Analysis, RFM Modeling, Data Imputation)