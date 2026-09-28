# FoodHub Order Analysis

## Project Overview

FoodHub is a food aggregator platform that connects customers with restaurants through an online ordering and delivery application.

As the number of restaurants and online food orders continues to grow, understanding customer demand, restaurant performance, delivery efficiency, and order behavior becomes increasingly important.

This project performs an **Exploratory Data Analysis (EDA)** on FoodHub order data to uncover patterns that can help the company:

- Understand restaurant and cuisine demand
- Analyze customer ordering behavior
- Evaluate delivery performance
- Understand customer ratings
- Estimate platform revenue
- Identify opportunities to improve customer experience

The analysis combines descriptive statistics, data cleaning, visualization, and multivariate analysis to translate raw order data into actionable business insights.

---

## Business Objective

The objective of this project is to analyze FoodHub's historical order data and answer key business questions related to:

- Customer ordering behavior
- Popular restaurants
- Cuisine demand
- Order costs
- Ratings
- Food preparation time
- Delivery time
- Weekday vs. weekend behavior
- Revenue generation
- Restaurant promotion opportunities

The final goal is to provide recommendations that can help FoodHub improve customer experience and business performance.

---

## Dataset

The dataset contains information about individual FoodHub orders.

| Feature | Description |
|---|---|
| `order_id` | Unique identifier for each order |
| `customer_id` | Unique identifier for the customer |
| `restaurant_name` | Name of the restaurant |
| `cuisine_type` | Cuisine ordered by the customer |
| `cost_of_the_order` | Cost of the order |
| `day_of_the_week` | Whether the order was placed on a weekday or weekend |
| `rating` | Customer rating out of 5 |
| `food_preparation_time` | Time taken by the restaurant to prepare the order |
| `delivery_time` | Time taken to deliver the food after pickup |

---

## Project Workflow

```text
Business Problem
      ↓
Data Understanding
      ↓
Data Quality Analysis
      ↓
Univariate Analysis
      ↓
Bivariate Analysis
      ↓
Multivariate Analysis
      ↓
Revenue Analysis
      ↓
Delivery Performance Analysis
      ↓
Customer & Restaurant Insights
      ↓
Business Recommendations
```

---

## Data Understanding

The dataset was first examined to understand its structure and quality.

The analysis included:

- Dataset dimensions
- Column data types
- Statistical summaries
- Missing-value checks
- Data-quality issues
- Unique values across important categorical variables

A key data-quality issue identified was the `rating` column.

There were **736 orders where the rating was recorded as `"Not given"`** rather than as a numeric value.

This required appropriate treatment before performing numerical analysis involving customer ratings.

---

## Data Cleaning

The `rating` variable contained both numerical ratings and `"Not given"` values.

Before performing rating-based analysis, the column was cleaned and converted into a suitable numerical format.

This ensured that subsequent visualizations and calculations involving ratings were accurate and did not fail because of mixed data types.

---

# Exploratory Data Analysis

## Univariate Analysis

Each important variable was analyzed individually to understand its distribution and characteristics.

The analysis included:

- Order cost distribution
- Cuisine frequency
- Restaurant order frequency
- Customer ordering frequency
- Weekday vs. weekend orders
- Customer ratings
- Food preparation time
- Delivery time

Visualizations included:

- Histograms
- Count plots
- Box plots

These visualizations helped identify common ordering patterns, popular cuisines, typical delivery times, and potential outliers.

---

## Restaurant Demand Analysis

Restaurant order counts were analyzed to identify the most frequently ordered restaurants on the FoodHub platform.

This helps FoodHub understand:

- Which restaurants receive the highest demand
- Which restaurants contribute heavily to platform activity
- Which restaurant partners may be suitable for promotional campaigns

---

## Cuisine Analysis

Cuisine categories were analyzed to understand customer preferences.

The analysis helped identify:

- Most popular cuisines
- Relative demand across cuisine types
- Opportunities for cuisine-specific promotions

Understanding cuisine demand can help FoodHub improve restaurant onboarding, promotions, and customer recommendations.

---

## Order Cost Analysis

The distribution of `cost_of_the_order` was analyzed to understand customer spending behavior.

This provides insight into:

- Typical order values
- High-value orders
- Customer spending patterns
- Revenue opportunities

Order value is particularly important because FoodHub earns revenue through commissions or margins on completed orders.

---

# Multivariate Analysis

Relationships between multiple variables were explored to understand how different factors interact.

The analysis included relationships between:

- Cuisine type and order cost
- Restaurant and ratings
- Cuisine and ratings
- Order cost and ratings
- Food preparation time and cuisine
- Delivery time and day of the week
- Customer ratings and delivery characteristics

Appropriate plots included:

- Box plots
- Bar charts
- Count plots
- Correlation heatmaps

---

## Rating Analysis

Customer ratings were analyzed after converting the rating column into a numerical format.

The analysis helped explore whether rating behavior was associated with:

- Restaurant
- Cuisine
- Order cost
- Preparation time
- Delivery performance

Customer ratings provide an important signal for understanding overall customer experience.

---

## Promotional Restaurant Analysis

The project identified restaurants meeting the criteria for potential promotional offers.

This allows FoodHub to identify restaurants that:

- Receive sufficient order volume
- Maintain strong customer ratings
- May benefit from promotional partnerships

Such analysis can support targeted promotions rather than offering incentives uniformly across every restaurant.

---

## Revenue Analysis

FoodHub earns revenue by collecting a margin on restaurant orders.

Based on the business rules provided in the analysis, the estimated net revenue generated was:

**$6,166.30**

This analysis demonstrates how order-level data can be translated directly into financial insights.

---

## Delivery Performance

Delivery performance was analyzed to understand how frequently customers experience long total order times.

Approximately **10.54% of orders took more than 60 minutes** from preparation through delivery.

Long order times can negatively affect customer experience and potentially influence ratings and repeat usage.

This makes delivery efficiency an important operational metric for FoodHub.

---

## Weekday vs. Weekend Delivery

Delivery behavior was compared between weekdays and weekends.

The analysis showed differences in delivery times between the two periods.

This may reflect factors such as:

- Traffic conditions
- Order volume
- Delivery-partner availability
- Restaurant workload

Understanding these differences can help FoodHub improve delivery staffing and operational planning.

---

# Key Business Insights

## 1. Restaurant Demand Is Concentrated

A relatively small set of restaurants receives a large share of orders.

### Business Implication

FoodHub can strengthen relationships with high-demand restaurants while also helping lower-volume restaurants improve visibility.

---

## 2. Cuisine Preference Can Guide Promotions

Certain cuisine categories receive considerably higher order volumes.

### Business Implication

FoodHub can use cuisine-level demand information for:

- Personalized recommendations
- Targeted promotions
- Restaurant acquisition
- Marketing campaigns

---

## 3. Customer Ratings Require Better Capture

A substantial number of orders have no recorded customer rating.

### Business Implication

Increasing rating participation can provide FoodHub with stronger data for evaluating restaurant quality and customer satisfaction.

---

## 4. Long Delivery Times Affect a Meaningful Share of Orders

Approximately **10.54% of orders exceed 60 minutes** in total processing and delivery time.

### Business Implication

FoodHub should monitor slow orders and identify whether delays originate from:

- Restaurant preparation
- Delivery assignment
- Pickup delays
- Travel time

---

## 5. Weekday and Weekend Operations Differ

Delivery performance varies between weekdays and weekends.

### Business Implication

Delivery staffing and operational strategies should account for differences in demand and delivery conditions throughout the week.

---

## 6. Restaurant Performance Can Support Targeted Promotions

Restaurants with strong ratings and sufficient order volumes can be identified through historical order data.

### Business Implication

FoodHub can allocate promotional spending toward restaurants that demonstrate strong customer satisfaction and demand.

---

## 7. Order Data Directly Supports Revenue Analysis

The analysis estimated approximately **$6,166.30 in platform revenue** based on the provided commission structure.

### Business Implication

Combining order behavior with revenue rules enables FoodHub to evaluate which customers, restaurants, cuisines, and order-value ranges contribute most to the business.

---

# Business Recommendations

## Recommendation 1 — Strengthen Partnerships With High-Demand Restaurants

Restaurants receiving consistently high order volumes should be treated as strategically important partners.

FoodHub can use:

- Promotional placements
- Joint offers
- Loyalty campaigns
- Exclusive discounts

to strengthen these relationships.

---

## Recommendation 2 — Use Cuisine Demand for Personalization

Cuisine preferences can be incorporated into recommendation and marketing strategies.

Customers can receive:

- Cuisine-specific promotions
- Restaurant recommendations
- Personalized offers

based on historical ordering behavior.

---

## Recommendation 3 — Improve Delivery Performance

Orders exceeding 60 minutes should be monitored closely.

FoodHub can analyze whether delays originate from restaurant preparation or delivery operations and use this information to improve:

- Delivery-partner allocation
- Pickup coordination
- Restaurant performance monitoring
- ETA estimates

---

## Recommendation 4 — Increase Customer Rating Participation

Since many orders have `"Not given"` ratings, FoodHub can encourage customers to provide feedback through:

- In-app reminders
- Simplified rating flows
- Small incentives
- Post-delivery notifications

More complete rating data would improve restaurant-quality analysis.

---

## Recommendation 5 — Optimize Weekend Operations

Since delivery behavior differs between weekdays and weekends, FoodHub should adjust delivery capacity based on historical demand patterns.

This can include:

- Increasing delivery-partner availability
- Improving peak-hour allocation
- Monitoring restaurant preparation capacity

---

## Recommendation 6 — Use Data for Targeted Restaurant Promotions

Promotions should be based on measurable restaurant performance rather than applied uniformly.

Relevant factors include:

- Order volume
- Customer ratings
- Cuisine popularity
- Revenue contribution

---

## Recommendation 7 — Monitor Revenue by Business Segment

Revenue analysis can be extended across:

- Restaurant
- Cuisine
- Customer
- Day of week
- Order-value range

This can help FoodHub identify where its strongest revenue opportunities exist.

---

# Executive Summary

This project performs an end-to-end exploratory analysis of FoodHub's online food-order data.

The analysis examined:

- Customer ordering patterns
- Restaurant demand
- Cuisine popularity
- Order costs
- Customer ratings
- Preparation time
- Delivery performance
- Revenue generation
- Weekday and weekend differences

A key data-quality issue was identified in the rating column, where **736 ratings were recorded as `"Not given"`** and required treatment before numerical analysis.

The analysis also found that approximately **10.54% of orders exceeded 60 minutes**, highlighting delivery efficiency as an important operational consideration.

Using the provided commission structure, FoodHub's estimated revenue from the analyzed orders was approximately **$6,166.30**.

Overall, the project demonstrates how exploratory data analysis can translate transactional data into actionable insights related to customer experience, restaurant strategy, operations, and revenue.

---

# Key Concepts Demonstrated

This project demonstrates practical application of:

- Exploratory Data Analysis
- Data Cleaning
- Missing / Non-Numeric Value Handling
- Statistical Summaries
- Univariate Analysis
- Bivariate Analysis
- Multivariate Analysis
- Histograms
- Count Plots
- Box Plots
- Correlation Heatmaps
- Customer Behavior Analysis
- Restaurant Demand Analysis
- Revenue Analysis
- Delivery Performance Analysis
- Business Insight Generation
- Data-Driven Recommendations

---

# Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Google Colab
- Jupyter Notebook

---

# Repository Structure

```text
foodhub-order-analysis/
│
├── README.md
├── FoodHub_Notebook.ipynb
├── FoodHub_Notebook.html
│
└── data/
    └── foodhub_order.csv
```

## Files

- `README.md` — Project overview, analysis, business insights, and recommendations
- `FoodHub_Notebook.ipynb` — Complete Google Colab notebook containing data exploration, visualization, analysis, and conclusions
- `FoodHub_Notebook.html` — Rendered version of the notebook for convenient viewing
- `data/` — FoodHub order dataset used for the analysis

---

# Conclusion

This project demonstrates how **Exploratory Data Analysis can transform transactional food-delivery data into meaningful business insights**.

By analyzing restaurant demand, cuisine preferences, customer spending, ratings, preparation times, delivery performance, and revenue, FoodHub can make more informed decisions across operations, marketing, restaurant partnerships, and customer experience.

The analysis highlights that improving delivery efficiency, strengthening relationships with high-demand restaurants, increasing customer feedback, and using targeted promotions can help FoodHub improve both customer satisfaction and business performance.