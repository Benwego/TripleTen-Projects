# Business Metrics Analysis: E-commerce User Activity

## Project Overview
In this project, I worked as a hypothetical junior analyst at an e-commerce company to analyze their raw user activity data. My task was to turn the company's transaction logs into actionable business metrics, focusing on building a conversion funnel, preparing data for cohort analysis, and calculating retention rates.

### Data Overview:
- The dataset contains event logs of user activities on the company's website, captured by the `raw_user_activity` tab.
- Each row represents an event by a user, including interactions such as product page views, shopping cart openings, and purchases.
- Columns in the dataset:
  - **user_id**: Unique customer IDs.
  - **event_type**: Type of user activity.
  - **category_code**: Category of the product involved.
  - **brand**: The brand of the product.
  - **price**: Price of the product (USD).
  - **event_date**: Date of the user activity.

---

## Part 1: Build a Conversion Funnel
### Objective:
The executive team wanted to understand how well the website is converting product page views into purchases.

### Tasks:
1. **Created a Conversion Funnel Pivot Table**:
   - Three stages of the funnel: product page views → cart opens → purchases.
   - Counted unique users at each stage.
   
2. **Calculated Conversion Rates**:
   - Added two new columns in the pivot table:
     - **Total Conversion Rate**: Overall conversion from product page views to purchases.
     - **Conversion Rate to the Next Step**: Conversion from each step to the next (e.g., views to cart opens, cart opens to purchases).
     
### Result:
- The funnel helped identify where drop-offs were occurring and provided a clearer picture of user engagement with the website.

---

## Part 2: Prepare Data for Cohort Analysis
### Objective:
The company wanted to build acquisition cohorts based on the month of a user’s first purchase and track cohort metrics over time.

### Tasks:
1. **Filtered and Isolated Purchases**:
   - Created a new tab, `purchase_activity`, containing only purchase event data (4,845 rows).

2. **Calculated First Purchase Dates**:
   - Used a pivot table to calculate the first purchase date for each user.
   - Used a `VLOOKUP` function to add the first purchase date to the `purchase_activity` sheet.

3. **Set Up Monthly Cohort Data**:
   - Added columns for `event_month`, `first_purchase_month`, and `cohort_age`.
   - Used the `TEXT()` function to format dates for cohort grouping and the `DATEDIF()` function to calculate the cohort's age in months.

### Result:
- Prepared the data for cohort analysis, which will help track user retention over time and understand how cohorts behave month by month.

---

## Part 3: Calculate Retention Rates
### Objective:
To calculate retention rates for each cohort, tracking how many users from each cohort made purchases in subsequent months.

### Tasks:
1. **Grouped Data into Cohorts**:
   - Used the `purchase_activity` data to create a cohort analysis pivot table.
   - Grouped users by the month of their first purchase and tracked their behavior over 4 months.

2. **Calculated Retention Rates**:
   - Created a new sheet, `retention_rates`, and calculated the retention rates for each cohort and each cohort age using a formula based on cohort sizes.

### Result:
- The retention rate calculation helped provide insights into how well the company retained users over time, and whether their marketing and engagement strategies were effective in bringing users back.

---

## Part 4: Organize and Document the Spreadsheet
### Objective:
To present the analysis in a polished and professional manner, ready for review by the executive team.

### Tasks:
1. **Filled in the Executive Summary**:
   - Summarized the key results from the `conversion_funnel` and `retention_rates` sheets.
   - Explained the assumptions made during the analysis and how the data was used.

2. **Reordered and Organized Sheets**:
   - Structured the spreadsheet in a logical order: Executive Summary → Analytical Results → Calculations → Raw Data.

3. **Formatted for Readability**:
   - Applied formatting best practices such as freezing rows, adding borders, and highlighting key calculations.
   - Ensured all numbers and dates were properly formatted and easy to interpret.

### Result:
- The spreadsheet was organized for clarity and usability, making it easy for the executive team to review and understand the analysis.

---

## Project Submission
- (https://docs.google.com/spreadsheets/d/1qYjkp7mRCmSnr5CGvSlpS84h9gsoEeKJtzBdaXUKR5Q/edit?usp=sharing))
- The link will provide view-only access to the spreadsheet, so reviewers can evaluate the project without making changes.

---

## Analysis and Assumptions:
### Conversion Funnel:
- The funnel stages were calculated based on user counts at each stage, showing drop-offs from product page views to purchases.

### Cohort Analysis:
- Cohorts were formed based on the first purchase date, with cohorts being tracked over four months to analyze retention patterns.
  
### Retention Rates:
- Retention rates were calculated by dividing the number of users who made a purchase in subsequent months by the total number of users in the cohort.
  
---

## Conclusion:
This project helped the company understand their user engagement better, highlighting key areas for improvement in their conversion process and user retention. By analyzing the data through conversion funnels and cohort retention, the company can make more informed decisions about marketing, product offerings, and customer engagement strategies.
