# Supermarket Customer Segmentation Analysis

## Project Overview

This project performs a strategic segmentation of a supermarket's customer base to identify key personas and uncover actionable insights for targeted marketing. Using a dataset of over 2,200 customers, this analysis moves beyond simple metrics to create a robust segmentation model based on both demographic data (Income) and behavioral data (Recency, Frequency, Monetary).

The final output is a strategic playbook and a mock-up for an interactive Tableau dashboard designed to help the marketing team make data-driven decisions to increase customer retention and lifetime value.

## Key Questions Answered

This analysis was designed to answer four core business questions:

1.  How can we segment customers based on their purchasing habits (RFM)?
2.  Which product categories are most popular with our most valuable segments?
3.  Which purchasing channels (Store, Web, Catalog) do different segments prefer?
4.  How effective have our past marketing campaigns been across different segments?

## Key Insights & Strategic Recommendations

Our analysis revealed a customer base split into two realities: a highly engaged, high-income niche and a large, untapped majority. The final playbook is built on three core strategies:

1.  **Activate the "Cherry-Pickers" (`Medium Income - Low Spender`):** Our largest growth opportunity. The strategy is to convert their deal-hunting, single-item trips into full-basket shopping trips using basket-based offers.
2.  **Cultivate the "Growth Engine" (`Medium Income - Medium Spender`):** Our largest customer segment. The strategy is to nurture their passion for premium products (especially wine) through targeted cross-selling and loyalty programs.
3.  **Insulate the VIPs (`High Income - High Spender`):** Our most valuable revenue stream. The strategy is to focus on retention and exclusivity through high-touch services like a "VIP Concierge," acknowledging that their primary need is convenience, not discounts.

## Technical Details

### Data Source

The dataset contains transactional and demographic information for supermarket customers from 2012-2014.

### Tools & Libraries

*   **Language:** Python 3
*   **Libraries:** pandas, NumPy, seaborn, matplotlib, plotly, statsmodels, scikit-learn
*   **Visualization:** Tableau

### Project Structure

The analysis follows a standard data science workflow:

1.  **Data Cleaning:** Handled missing values (Income), removed outliers, corrected data types (`Dt_Customer`), and standardized categorical variables (`Education`, `Marital_Status`).
2.  **Feature Engineering:** Created new, insightful columns for analysis, including:
    *   `Age` (calculated relative to the dataset's timeframe)
    *   `Family_Size` & `Is_Parent`
    *   `Monetary` (Total Spend) & `Frequency` (Total Purchases)
3.  **Segmentation:**
    *   Developed a 3x3 segmentation matrix by classifying customers into `Income_Level` (Low, Medium, High) and `RFM_Spender_Level` (Low, Medium, High).
    *   `RFM_Spender_Level` was calculated using a data-driven, quartile-based RFM model.
4.  **Modeling & Analysis:**
    *   Generated detailed **Customer Dossiers** for each of the 9 segments.
    *   Analyzed **Spending Composition**, **Channel Preference**, and **Campaign Acceptance Rates** for each segment.
    *   Calculated **Customer Lifetime Value (CLV)** and ran simulations to quantify the financial impact of proposed marketing strategies.
    *   Used **Linear Regression** to confirm the primary drivers of customer spending.
5.  **Dashboarding:** Designed a mock-up for a four-part interactive Tableau dashboard to allow for dynamic exploration of the segments.

### How to Run

1.  Ensure you have the required Python libraries installed.
2.  Place the `Supermarket Customers.csv` file in the same directory as the Jupyter Notebook.
3.  Run the cells sequentially in the main analysis notebook (`Your_Notebook_Name.ipynb`) to replicate the analysis.
4.  The final, cleaned, and segmented data is exported to `supermarket_customers_segmented.csv`, which can be used as the data source for the Tableau dashboard.
