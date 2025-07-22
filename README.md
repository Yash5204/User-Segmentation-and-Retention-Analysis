# 📈 User-Segmentation-and-Retention-Analysis

## Project Overview

This project provides a comprehensive analysis of user behavior data from a multi-category e-commerce store, focusing on understanding customer retention, identifying churn patterns, and segmenting the user base for targeted marketing and product strategies. Leveraging a real-world dataset of over 25 million events, this analysis aims to translate raw behavioral data into actionable business intelligence, ultimately driving growth and improving customer lifetime value.

## 🎯 Objectives

* **Identify User Churn Patterns:** To analyze user activity and pinpoint critical drop-off points within the user lifecycle.
* **Segment Users:** To group customers into meaningful and actionable segments based on their historical Recency, Frequency, and Monetary (RFM) value.
* **Quantify Churn Risk:** To calculate and visualize specific churn rates for each defined customer segment, allowing for prioritized interventions.
* **Visualize Key Insights:** To present complex data trends and user behavior patterns through intuitive and impactful visualizations, including cohort heatmaps and user funnels.
* **Formulate Actionable Recommendations:** To provide data-driven strategies that the e-commerce platform can implement to improve user retention and drive conversion rates.

---

## 🗄️ Dataset

The analysis utilizes a **month-long (November 2019)** dataset of e-commerce user behavior from a multi-category store, comprising over **25 million events** (sampled from a much larger original dataset due to computational and memory constraints).

* **Source:** [E-commerce Behavior Data from Multi-category Store - Kaggle](https://www.kaggle.com/datasets/mikhailkarmazin/ecommerce-behavior-data-from-multi-category-store) (Specifically, the `2019-Nov.csv` file)
* **Key Fields:** `event_time`, `event_type`, `product_id`, `category_id`, `category_code`, `brand`, `price`, `user_id`, `user_session`.

## 🛠️ Tools & Technologies

* **Python:** Programming language for core data manipulation and analysis.
    * `pandas`: Fundamental library for data structuring, manipulation, and analysis (DataFrames).
    * `numpy`: Provides support for numerical operations and array computations.
    * `seaborn`: A high-level statistical data visualization library, built on Matplotlib, for creating informative and attractive plots.
    * `matplotlib.pyplot`: The foundational plotting library for static visualizations.
    * `datetime`: Python's built-in module for efficient handling of date and time objects.
    * `plotly.express`: A high-level API for creating interactive and dynamic data visualizations, particularly effective for funnels.
    * `operator.attrgetter`: Used for efficient attribute retrieval in specific data processing steps.
* **Jupyter Notebook:** For an interactive, reproducible, and cell-by-cell analysis workflow.
* **SQL Concepts:** Though not explicitly in the notebook code, the data aggregation and querying mindset is fundamental to this analysis, reflecting skills in database interaction.

---
## 📊 Key Findings & Insights

* **Dominant Non-Purchaser Segment:** Approximately **92.32%** of all unique users acquired in November did not make a single purchase, indicating a major challenge in first-time conversion.
* **Steep Early Churn:** The overall funnel analysis revealed a dramatic drop-off, with only **5.83%** of acquired users remaining active by Day 7 of their lifecycle. The cohort heatmap further illustrated this with individual cohorts experiencing a significant drop from 100% to ~16-17% by Day 2.
* **High Churn in Valuable Segments:**
    * **100% of 'High Value, At Risk' users** (who were valuable purchasers but haven't been recent) were identified as churned based on the 7-day inactivity threshold.
    * **~73% of 'Promising New' users** (recent, some purchases) also churn within 7 days, highlighting a need for improved early-lifecycle nurturing.
* **Core Retained Segments:** 'Champions' showed 0% churn, 'Top Spenders' (~13.5% churn), and 'Loyal Customers' (~14.4% churn), confirming these segments as the most valuable and sticky.
* **Overall Retention Challenge:** By Day 28, only **1.00%** of the initially acquired users remained active, underscoring the challenge of building sustained long-term engagement.

## 💡 Actionable Recommendations

Based on these insights, the e-commerce platform should consider:

1.  **Optimize Onboarding & First-Purchase Conversion:** Focus efforts on the **~92% Non-Purchaser segment** and the **~73% 'Promising New' segment's** early lifecycle. Implement A/B tests for improved welcome flows, targeted first-purchase incentives, and clear value proposition communication within the first 7 days.
2.  **Proactive Win-Back for 'High Value, At Risk' Customers:** Given their 100% churn rate and high past value, develop immediate, personalized re-engagement campaigns (e.g., exclusive discounts, product recommendations based on past purchases) to reactivate this critical group.
3.  **Enhanced Retention for 'Engaged Buyers':** With a 53% churn rate, this segment needs mid-lifecycle nurturing. Consider loyalty programs, push notifications about new arrivals in their preferred categories, or personalized content based on Browse history.
4.  **Sustain Engagement for Top Tiers:** Implement VIP programs, early access to sales, or exclusive content for 'Champions', 'Top Spenders', and 'Loyal Customers' to foster continued loyalty and advocacy.

---

## 🖼️ Visualizations

### Daily User Retention Heatmap
<img width="1600" height="1000" alt="cohort_heatmap_full" src="https://github.com/user-attachments/assets/352630ca-9327-4b09-9176-cd54d9257654" />

### Key Daily User Retention Heatmap
<img width="1000" height="1200" alt="key_retention_heatmap" src="https://github.com/user-attachments/assets/069b02ce-71cd-45ce-aa37-36cf73d738ae" />

### RFM Segment Distribution
<img width="1000" height="700" alt="rfm_segment_distribution" src="https://github.com/user-attachments/assets/b9cd0063-afdd-4767-8a26-4cc13bdaa528" />

### Churn Rate by Segment
<img width="1000" height="700" alt="churn_rate_by_segment" src="https://github.com/user-attachments/assets/5a893617-a17f-40b7-8ef9-4ec555b5cad8" />

### User Drop-off Funnel (with Percentages)
<img width="1377" height="335" alt="image" src="https://github.com/user-attachments/assets/3b5dd0cd-f71a-46fd-a1e8-2bbe28fe1b9e" />

*(Note: This is a static image of an interactive Plotly chart. The live interactive version can be viewed by running the Jupyter Notebook locally.)*

---

## 🚀 How to Run

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/y/User-Segmentation-and-Retention-Analysis.git]((https://github.com/Yash5204/User-Segmentation-and-Retention-Analysis))
    cd User-Segmentation-and-Retention-Analysis
    ```
2.  **Install Dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn plotly jupyter
    ```
  
3.  **Download Data:** The raw data (`2019-Nov.csv`) is too large to be directly hosted on GitHub. Please download it from the [Kaggle Dataset Page](https://www.kaggle.com/datasets/mikhailkarmazin/ecommerce-behavior-data-from-multi-category-store) and place it in a `data/` folder within the cloned repository.
   
4.  **Run Jupyter Notebook:**
    Open the `User_Retention_Analysis.ipynb` file in your browser. Ensure to run all cells sequentially from top to bottom.

## 🔭 Future Work

* Integrate additional data sources (e.g., customer demographics, marketing campaign data) for richer segmentation and deeper insights.
* Develop and implement a **churn prediction model** using machine learning algorithms to proactively identify users at risk before they disengage.
* Perform A/B testing on recommended strategies (e.g., different onboarding flows, re-engagement campaigns) and rigorously measure their impact on retention and conversion rates.
* Expand RFM to include **product-specific segmentation** or explore the impact of `user_session` behavior on conversion funnels in more detail.
* Create a fully interactive dashboard in Power BI, pulling in the processed `user_funnel.csv` and potentially other aggregated data from the analysis.

---

## 🚀 Methodology & Analysis Breakdown

The project follows a structured approach, progressing through robust data preparation, advanced analytical techniques, and compelling visualization to derive actionable insights.

### Environment Setup & Library Imports

We begin by importing the core libraries used throughout the project:

-   `warnings`: Configured to suppress specific `RuntimeWarning`, `FutureWarning`, and timezone-related warnings, ensuring cleaner notebook output.
-   `pandas`: The fundamental library for efficient data manipulation and analysis, crucial for working with DataFrames.
-   `numpy`: Provides support for numerical operations, often used in conjunction with `pandas` for mathematical computations.
-   `seaborn`: A high-level statistical data visualization library built on `matplotlib`, used to create aesthetically pleasing and informative plots. A 'viridis' color palette is set as default for consistent visualization.
-   `matplotlib.pyplot`: The core plotting library providing a comprehensive interface for creating static visualizations.
-   `datetime`: Python's built-in module for handling date and time objects, used for various time-based calculations.
-   `plotly.express`: A high-level API for generating interactive data visualizations, particularly useful for dynamic funnel charts.
-   `operator.attrgetter`: Imported for specific, efficient attribute retrieval, which can be useful in custom sorting or data processing operations.

This initial setup ensures the notebook runs cleanly, has all necessary tools available, and is ready for comprehensive user event analytics.

### Initial Data Overview & Quality Check

After loading and sampling the dataset, a crucial first step is to perform an extensive initial data overview. This helps in understanding the dataset's structure, identifying key characteristics, and uncovering potential data quality issues before proceeding with analysis.

This section provides:

-   **Temporal Scope Confirmation:** Verification of the exact date range covered by the `event_time` column, confirming the dataset is specifically for November 2019.
-   **Scale Assessment:** Counts of the total number of events and unique users within the sampled dataset, providing an understanding of the data's overall magnitude.
-   **Event Type Distribution:** A breakdown of how frequently each `event_type` (e.g., 'view', 'cart', 'purchase') occurs, offering immediate insights into general user activity patterns.
-   **Dimensionality Check:** Display of the DataFrame's shape (number of rows and columns).
-   **Data Type Verification:** A summary of the data type for each column, ensuring that critical columns like `event_time` are correctly parsed as datetime objects for time-series analysis.
-   **Missing Values Identification:** A count of null values per column, highlighting any missing data that requires cleaning or imputation strategies.
-   **Cardinality Analysis:** The number of unique values for each column, which is essential for understanding the diversity of categorical features and validating identifier columns (like `user_id`, `product_id`).

This comprehensive initial inspection forms the foundation for informed data cleaning and subsequent analytical steps.

### Data Cleaning and Memory Optimization

This phase focuses on refining the dataset by addressing identified data quality issues and significantly enhancing computational efficiency. This is crucial for handling large datasets effectively and ensuring the reliability of subsequent analyses.

Key steps performed include:

-   **Handling Missing Values:**
    * A very small number of rows with missing `user_session` values were explicitly identified and removed, as their impact on the overall dataset (25 million entries) was negligible.
    * For columns with a more substantial amount of missing data (`category_code` and `brand`), `NaN` values were strategically filled with the string 'Unknown'. This approach preserves the integrity of the rows, allowing all events to contribute to the analysis, while explicitly categorizing the missing information.
-   **Zero Price Investigation:**
    * An investigation into `event_time`s where `price` was `0.0` was conducted. It was confirmed that these zero prices were consistently associated with 'view' and 'add_to_cart' event types, indicating they are logical and expected data points rather than errors (as these actions do not directly incur a cost).
-   **Memory Optimization:**
    * A significant reduction in the DataFrame's memory footprint (approximately 60%) was achieved. This optimization is vital for improving processing speed and preventing memory-related issues when working with large datasets.
    * **Downcasting Numerical Types:** Integer columns such as `product_id`, `category_id`, and `user_id` were converted to smaller, more memory-efficient integer types (`int32`) where their value range permitted.
    * **Categorical Type Conversion:** String-based 'object' columns with a limited number of unique values (low cardinality), like `event_type`, `category_code`, and `brand`, were converted to Pandas' `category` data type. This highly efficient data type stores unique values once and uses integer codes internally, leading to substantial memory savings.

### Feature Engineering for Cohort Analysis (Part 1: Date Derivations)

This phase focuses on deriving essential date-based features that are foundational for conducting robust cohort analysis. These features allow us to define user cohorts and track their activity relative to their initial engagement.

Key derivations performed include:

-   **Event Date Normalization:** The `event_time` column, which contains precise timestamps, is floored to the nearest day (`.dt.floor('D')`). This creates a new `event_date` column that represents just the date part (e.g., 2019-11-15 00:00:00), ensuring consistency for date-based comparisons while preserving the `datetime64[ns]` data type critical for Pandas' time-series functionalities.
-   **First Active Date (Cohort Definition):** For each unique user, their `first_active_date` is determined by finding the minimum `event_date` associated with that user. This date serves as the user's "cohort entry point" – the specific day they first became active on the platform. This derived date is then merged back into the main DataFrame, linking every event to its user's unique cohort.
-   **Last Active Date (Recency Basis):** Similarly, for each unique user, their `last_active_date` is calculated by finding the maximum `event_date`. This metric is crucial for the "Recency" component of RFM analysis, as it indicates how recently a user has interacted with the platform. This date is also merged back into the main DataFrame.

These derived date features are critical for segmenting users into cohorts and for calculating key retention and Recency metrics in subsequent analytical steps.

### Feature Engineering for Cohort Analysis (Part 2: Period Calculations)

Building upon the derived date features, this phase calculates key metrics essential for tracking user engagement and defining cohort-specific activity periods. These calculations are fundamental for constructing the cohort retention matrix.

Key calculations performed include:

-   **Cohort Day:** The `cohort_day` is extracted as the day of the month from each user's `first_active_date`. This categorizes users by the specific calendar day in November they first became active (e.g., users joining on November 1st are in Cohort Day 1).
-   **Active Days (Lifecycle Progression):** The `active_days` metric represents the number of days elapsed between a user's `first_active_date` and the `event_date` of any given event. A value of 0 means the event occurred on their first day (Day 1 of their lifecycle), 1 means Day 2, and so on. This precisely tracks how many days into their lifecycle an event occurred.
-   **Cohort Period:** For daily retention analysis, the `active_days` directly serves as the `cohort_period`. This standardized term indicates a user's stage within their engagement lifecycle (e.g., `cohort_period = 0` signifies Day 1 activity, `cohort_period = 6` signifies Day 7 activity).

These features are crucial for grouping user activities by their initial join date and observing their behavior over successive days, forming the basis for the retention heatmaps.

### Cohort Analysis Calculation

This phase aggregates the meticulously prepared data to construct the core **cohort retention matrix**. This matrix is the numerical foundation for understanding user retention rates across various cohorts and over time.

Key steps involved are:

-   **Aggregating User Counts:** Users are grouped by their `first_active_date` (defining each cohort) and their `cohort_period` (days since first activity). For each unique combination, the number of distinct `user_id`s is counted. This provides the raw number of users from a specific cohort who were active on a particular day of their lifecycle.
-   **Pivoting for Matrix Format:** The aggregated counts are then transformed into a pivot table. The `first_active_date` becomes the index (rows), representing each daily cohort. The `cohort_period` forms the columns (representing days into the user's lifecycle: Day 1, Day 2, etc.). The values within the table are the `num_users` active in that specific cohort and period.
-   **Calculating Cohort Sizes:** The initial size of each cohort (the total number of users who joined on a specific `first_active_date`) is extracted. This is crucial as it serves as the baseline for calculating retention percentages.
-   **Computing Retention Percentages:** Each cell in the raw cohort pivot table is divided by its corresponding `cohort_size` (the initial number of users in that cohort). The result is then multiplied by 100 to express retention as a percentage. This `retention_matrix` clearly shows the percentage of users from each cohort who remained active in subsequent days.

This matrix is then used for visual analysis, revealing patterns of user stickiness and drop-off over time.

### Cohort Analysis Visualization

This phase creates heatmaps to visually represent user retention patterns, making complex data easily interpretable.

Key aspects of this visualization include:

-   **Full Daily Retention Heatmap:** A detailed heatmap was generated to show the percentage of users retained across all cohorts and daily periods. This visually highlights the initial steep drop-off and the subsequent retention curve.
-   **Key Retention Heatmap:** A more focused heatmap was created to specifically highlight retention rates at critical milestones: Day 1, Day 2, Day 7, and Day 30 (where data permits). This offers a quick glance at short-term and mid-term retention performance.
-   **Heatmap Generation:** `seaborn.heatmap` is used, where each cell's color intensity represents the retention rate (percentage).
-   **Annotations & Color Mapping:** Percentages are displayed within cells, and a 'YlGnBu' colormap is applied, where darker shades indicate higher retention.
-   **Readability Enhancements:** Titles, axis labels, and layout adjustments ensure clarity.
-   **Saving Plots:** All generated heatmaps are saved as PNG images (`cohort_heatmap_full.png`, `key_retention_heatmap.png`) for inclusion in the project's documentation.

This heatmap serves as a cornerstone for understanding the overall daily retention performance and identifying key periods of user drop-off.

### RFM Calculation (Core Metrics)

This section marks the beginning of the Recency, Frequency, and Monetary (RFM) analysis, a powerful customer segmentation technique. The goal here is to compute the three core RFM metrics for each unique user in the dataset.

Key steps involved are:

-   **Defining Snapshot Date:** A `snapshot_date` is established as the day immediately following the last event recorded in the dataset. This fixed point in time is crucial for accurately calculating "Recency," as it defines how recently a user's last activity occurred relative to the end of our observation period.
-   **Aggregating RFM Metrics per User:**
    * **Recency:** Calculates the number of days between the `snapshot_date` and the user's latest recorded `event_time`. Lower Recency indicates more recent activity.
    * **Frequency:** Counts the total number of events (interactions) for each user, capturing overall engagement.
    * **Monetary:** Sums the `price` of all 'purchase' events for each user, reflecting actual monetary value contributed. Users with no purchases are assigned `0`.
-   **Initial RFM Data Review:** The resulting `rfm_df` is inspected to validate calculated metrics and understand their distributions.

### RFM Calculation (Adding Purchase-Specific Frequency)

This section refines the Frequency metric in the RFM model by specifically focusing on the number of *purchase* events per user. This provides a more precise measure of actual buying behavior, distinct from overall engagement (total events).

Key steps in this refinement are:

-   **Isolating Purchase Events:** The original DataFrame is filtered to create a new DataFrame containing only 'purchase' events.
-   **Calculating Purchase Frequency:** For each unique user, the total number of purchase events is counted, forming the `Frequency_Purchases` column.
-   **Merging into RFM DataFrame:** This new purchase frequency data is merged into the existing `rfm_df`. Users with no purchases are correctly assigned a `Frequency_Purchases` of `0`.
-   **Data Type Conversion:** The `Frequency_Purchases` column is converted to an integer type for consistency and efficiency.

This enhanced `Frequency_Purchases` metric provides a more nuanced understanding of a user's transactional activity, which is crucial for building more accurate and actionable customer segments.

### RFM Scoring (Assigning R, F, M Scores)

This phase transforms the raw Recency, Frequency, and Monetary metrics into standardized scores, typically on a scale of 1 to 5. This scoring allows for easier comparison and combination of the metrics to form distinct customer segments.

The scoring process includes:

-   **Recency Score (R_Score):** Users are divided into 5 equal groups (quintiles). A reverse scoring mechanism is applied: lowest Recency (most recent) gets score 5 (best), highest Recency (least recent) gets score 1 (worst).
-   **Frequency Score (F_Score):** This score is based on `Frequency_Purchases`. Only users with positive purchase frequency are scored into 5 quintiles (1-5); non-purchasing users are explicitly assigned a score of `0`.
-   **Monetary Score (M_Score):** Similar to Frequency, this score is based on `Monetary` value. Only users with positive monetary contribution are scored into 5 quintiles (1-5); non-purchasing users are explicitly assigned a score of `0`.

After scoring, the distribution of scores for R, F, and M is displayed, showing the proportion of users in each score bucket.

### RFM Segmentation (Categorizing Users)

This phase combines the individual Recency, Frequency (purchases), and Monetary scores into a single RFM score and then applies a custom logic to categorize users into actionable business segments. This allows for tailored marketing and product strategies based on customer value and behavior.

The process involves:

-   **Combined RFM Score:** The individual R, F, and M scores are concatenated into a single string (e.g., '555' for a top-tier customer, '120' for a customer with low Recency, moderate Frequency, and no Monetary value).
-   **Custom Segmentation Logic:** A Python function is defined with a series of conditional rules that assign each user to a specific segment based on their RFM scores. Segments are ordered from generally most distinct/high-priority (e.g., 'Champions', 'Loyal Customers', 'Top Spenders') to less specific/lower value (e.g., 'Lapsed Low-Value', 'Churned Purchasers', 'Other Segment'). The 'Non-Purchaser' segment is identified first, capturing all users with a `M_Score` of `0`.
-   **Segment Assignment:** The custom segmentation function is applied to the DataFrame, creating a new 'Segment' column.
-   **Segment Distribution Analysis:** The count of users in each segment is displayed, providing a clear overview of the size and proportion of each customer group.
-   **Segment Validation (Mean RFM Values):** The average Recency, Frequency (total events), Purchase Frequency, and Monetary values are calculated for each segment. This step is critical for validating that the defined segments genuinely reflect the intended behavioral characteristics and value profiles.

This segmentation process transforms raw RFM scores into actionable customer groups, enabling tailored marketing and product initiatives.

### RFM Segment Distribution Visualization

This section visualizes the distribution of users across the defined RFM segments and quantifies their proportions. This provides an immediate and clear understanding of the composition of the customer base, highlighting the relative sizes of each segment.

The visualization includes:

-   **Bar Chart Generation:** A `seaborn.countplot` is used to create a horizontal bar chart, where each bar represents an RFM segment, and its length corresponds to the number of users within that segment.
-   **Ordering and Coloring:** Segments are ordered by their size (from largest to smallest) for easy comparison, using a 'viridis' color palette.
-   **Readability Enhancements:** The plot includes a descriptive title and clear axis labels.
-   **Saving the Plot:** The generated chart is saved as a PNG image (`rfm_segment_distribution.png`) for inclusion in the project's documentation.
-   **Percentage Distribution:** The exact percentage of users falling into each RFM segment is calculated and printed, providing a precise quantitative breakdown.

This visualization and its accompanying percentage breakdown are crucial for quickly grasping the overall customer landscape and prioritizing strategies for different user segments.

### Churn Rate Analysis by Segment (Quantification)

This section quantifies the churn rate within each of the defined RFM segments, providing precise, actionable insights into which customer groups are most susceptible to churn. This analysis directly links user behavior segments to their churn likelihood.

The process involves:

-   **Defining Churn Threshold:** A `churn_threshold_days` is set (e.g., 7 days). A user is considered 'churned' if their `Recency` (days since last activity) exceeds this threshold, implying a period of inactivity.
-   **Creating Churn Flag:** A new binary column, `is_churned`, is added to the RFM DataFrame. It is set to `1` for users identified as churned and `0` otherwise.
-   **Calculating Segment Churn Rates:** The DataFrame is grouped by the 'Segment' column, and the mean of the `is_churned` flag is calculated for each group. Results are converted to percentages and sorted in descending order to highlight the most vulnerable segments.
-   **Displaying Results:** A sample of the DataFrame with the new `is_churned` flag is printed. The calculated churn rates (in percentage) for each segment are then displayed, providing a clear quantitative overview of churn risk across the customer base.

This quantification of churn by segment is crucial for prioritizing churn prevention and re-engagement strategies for the most at-risk and valuable customer groups.

### Churn Rate Analysis by Segment (Visualization)

This section provides a clear and impactful visualization of the churn rates for each RFM segment, complementing the quantitative analysis. This visual representation quickly highlights which customer groups are most affected by churn and thus require immediate attention.

The visualization includes:

-   **Bar Plot Generation:** A `seaborn.barplot` is used to create a horizontal bar chart, with each bar representing an RFM segment and its length corresponding to the calculated churn rate (in percentage).
-   **Ordering and Coloring:** Segments are ordered from highest to lowest churn rate, using a 'coolwarm' color palette.
-   **Readability Enhancements:** The plot includes a descriptive title (with the churn threshold), clear axis labels, and the X-axis limit set from 0 to 100% for accurate visual comparison.
-   **Saving the Plot:** The generated bar chart is saved as a PNG image (`churn_rate_by_segment.png`) for inclusion in the project's documentation.

This visualization is a powerful tool for communicating the churn insights to stakeholders, enabling them to prioritize resources for customer retention and win-back campaigns effectively.

### Overall Funnel Analysis (Data Preparation)

This section prepares the data for a high-level funnel analysis, providing an aggregated view of user drop-off from acquisition through key weekly milestones. Unlike cohort analysis which tracks individual cohorts, this funnel summarizes the overall retention across all users acquired during the observed period.

The data preparation steps include:

-   **Total Users Acquired:** The top of the funnel is defined by calculating the total number of unique users whose first activity occurred within the entire month of November.
-   **Weekly Active User Counts:** For key weekly milestones (Day 7, Day 14, Day 21, and Day 28 of a user's lifecycle), the total number of users active on those specific days (across all cohorts) is calculated. Missing data for later periods (due to the 1-month dataset) is handled gracefully.
-   **Funnel DataFrame Creation:** A new DataFrame is constructed, explicitly listing each funnel 'Stage' (e.g., 'Users Acquired (Nov)', 'Active on Day 7') and its corresponding `User_Count`.
-   **Retention Rate Calculation:** A `Retention_Rate (%)` column is added, showing the percentage of users remaining at each stage relative to the initial acquired user base.
-   **CSV Export:** The prepared funnel data is saved to a CSV file (`user_funnel.csv`), making it accessible for further analysis or integration into external tools like Power BI.

This prepared `funnel_df` serves as the foundation for visualizing the overall user drop-off and identifying the most significant points of attrition.

### Funnel Conversion Visualization

This section focuses on visualizing the user drop-off funnel, transforming the raw counts and retention rates into clear, interactive chart. This visualization is highly effective for quickly grasping user attrition patterns.

-   **Funnel with Percentages:**
    * A second interactive funnel chart is generated, similar to the first, but with a key enhancement: the text displayed on each bar is the `Retention_Rate (%)` for that stage.
    * This version provides an immediate visual representation of the percentage drop-off at each step, making the overall funnel conversion rates strikingly clear. This chart is also saved as a static PNG image (`plotly_funnel_with_percentages.png`).

This interactive funnel visualization is powerful tools for communicating the overall user retention challenges and highlighting the most significant points of attrition in the user journey.

---

## 📞 Connect with Me

* **LinkedIn:** [https://linkedin.com/Yashdtu]
* **GitHub:** [https://github.com/Yash5204]

---
