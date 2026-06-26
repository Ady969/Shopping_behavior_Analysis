# 🛒 Customer Shopping Behavior & Loyalty Analytics

## 🎯 1. Business Problem Statement
The retail management team has noticed stagnating revenue growth and unpredictable sales fluctuations across different seasons. The marketing and inventory teams are struggling with the following key challenges:
- **Low Retention:** Inability to differentiate spending patterns between loyal subscribers and one-time shoppers.
- **Untargeted Marketing:** Marketing budgets are wasted on generic ads instead of demographic-specific targeting (Age & Gender).
- **Inventory Mismatch:** Lack of data-driven insights into which age groups and genders buy specific sizes or categories across different seasons.

**Project Objective:** Build an end-to-end data pipeline using **Python (Pandas)** for data auditing and **Power BI** for interactive dashboards to decode customer behavior, optimize inventory, and improve subscription loyalty.

---

## 🛠️ 2. Tech Stack Used
- **Data Auditing & Cleaning:** Python 3 (Google Colab)
- **Libraries:** Pandas, NumPy
- **Data Visualization & Analytics:** Power BI Desktop
- **Formula Language:** DAX (Data Analysis Expressions)
- **AI Copilot:** Workik AI (for query generation & code optimization)

---

## 💻 3. Python Solution (Data Auditing & Cleaning)
Before loading the data into Power BI, Python was used to ensure data integrity and perform initial exploratory data analysis (EDA).

### Key Code Operations:
1. **Data Integrity Check:** Handled missing values using `df.isnull().sum()` to avoid biased calculations.
2. **KPI Baseline:** Calculated overall Total Revenue, Average Purchase Amount, and Unique Customer counts.
3. **Deep-Dive Segmentation:** Grouped purchase amounts by Gender and custom Age Bins (`18-30`, `31-50`, `51+`) using Pandas grouping logic.

*You can find the full executable notebook file (`.ipynb`) in this repository.*

---

## 📊 4. Power BI Interactive Dashboard
The raw data was transformed into a multi-perspective interactive dashboard. 

### Key Analytics Engineered:
- **Total Revenue Card:** Direct business health monitor.
- **Sales Contribution by Gender (Pie Chart):** Clear visual of which gender drives sales.
- **Revenue by Age Group (Clustered Column Chart):** Created via a custom DAX formula:
  ```dax
  Age Group = 
  SWITCH (
      TRUE (),
      'customer_shopping_behavior_1'[Age] <= 30, "18-30",
      'customer_shopping_behavior_1'[Age] <= 50, "31-50",
      "51+"
  )
  ```
- **Customer Satisfaction (Horizontal Bar Chart):** Measures Average Review Rating across subscription statuses.
- **Seasonal Slicer (Dynamic Buttons):** Allows stakeholders to filter the entire dashboard by Fall, Spring, Summer, or Winter dynamically.

<img width="1287" height="721" alt="image" src="https://github.com/user-attachments/assets/7aa4c265-af78-4807-bb9c-2603e3c5c9db" />


---

## 💡 5. Data-Driven Business Decisions & Future Recommendations
Based on the dashboard analytics, here are the strategic recommendations for the business:

1. **Targeted Female Campaigns:** If the data shows higher spending from female demographics, shift 60% of the marketing budget toward personalized female catalog promotions.
2. **Age-Based Inventory Optimization:** The `31-50` age segment shows unique seasonal trends. Inventory teams should stock popular sizes/colors based on this segment's preference ahead of peak seasons (e.g., Summer/Winter).
3. **Subscription Program Revamp:** Since subscribers and non-subscribers show closely matching average ratings (~3.8 to 3.9), the product quality is consistent, but subscription benefits (discounts, exclusive shipping) need to be marketed aggressively to convert high-spending non-subscribers.

---
