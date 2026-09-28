# FoodHub Order Analysis

## Project Overview

FoodHub is a food aggregator platform that connects customers with restaurants through an online ordering and delivery application.

As the number of restaurants and online food orders continues to grow, understanding customer demand, restaurant performance, delivery efficiency, ratings, and order behavior becomes increasingly important.

This project performs an **Exploratory Data Analysis (EDA)** on FoodHub order data to identify business patterns and provide actionable recommendations that can help improve customer experience, restaurant performance, operational efficiency, and revenue opportunities.

---

## Business Objective

The objective of this project is to analyze FoodHub's historical order data and answer key business questions related to:

- Customer ordering behavior
- Popular restaurants
- Cuisine demand
- Order costs
- Customer ratings
- Food preparation time
- Delivery time
- Weekday vs. weekend behavior
- Revenue generation
- Restaurant promotion opportunities

The final goal is to translate transaction-level data into practical recommendations for operations, marketing, restaurant partnerships, and customer engagement.

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
- Unique values across important categorical variables
- Data-quality issues

A key data-quality issue identified was the `rating` column.

There were **736 orders where the rating was recorded as `"Not given"`** rather than as a numeric value.

This issue was handled before performing numerical analysis involving customer ratings.

---

## Data Cleaning

The `rating` variable contained both numerical values and `"Not given"` entries.

Before performing rating-based analysis, the column was cleaned and converted into a suitable numerical format.

This ensured that subsequent calculations and visualizations involving ratings were accurate.

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

These visualizations helped identify order patterns, cuisine preferences, delivery behavior, and potential operational issues.

---

## Restaurant Demand Analysis

Restaurant order counts were analyzed to identify the most frequently ordered restaurants on the platform.

This helps FoodHub understand:

- Which restaurants receive the highest demand
- Which restaurants contribute heavily to platform activity
- Which restaurant partners could be prioritized for promotions and strategic partnerships

---

## Cuisine Analysis

Cuisine categories were analyzed to understand customer preferences and demand patterns.

The analysis showed particularly strong demand and ratings for cuisines such as:

- American
- Japanese
- Italian

Premium cuisines such as:

- French
- Thai
- Spanish

also present opportunities for differentiated marketing and higher-value customer targeting.

---

## Order Cost Analysis

The distribution of `cost_of_the_order` was analyzed to understand customer spending behavior.

This provides insight into:

- Typical order values
- Higher-value orders
- Customer spending patterns
- Potential segmentation opportunities

Order value is especially important because FoodHub earns revenue through commissions or margins on completed orders.

---

# Multivariate Analysis

Relationships between important business variables were analyzed to understand how different factors interact.

The analysis included relationships between:

- Cuisine type and order cost
- Restaurant and ratings
- Cuisine and ratings
- Order cost and ratings
- Food preparation time and cuisine
- Delivery time and day of the week
- Customer ratings and delivery characteristics

Appropriate visualizations included:

- Box plots
- Bar charts
- Count plots
- Correlation heatmaps

---

## Rating Analysis

Customer ratings were analyzed after converting the rating column into numerical format.

A large proportion of orders were unrated, limiting the completeness of restaurant and service-quality analysis.

Nearly **40% of orders did not contain a rating**.

This represents an important opportunity for FoodHub to improve the quality of customer-feedback data.

---

## Promotional Restaurant Analysis

The project identified restaurants that met criteria for promotional offers based on a combination of:

- Order volume
- Customer ratings
- Overall demand

High-performing restaurants such as **Shake Shack** and **Blue Ribbon Sushi Izakaya** provide useful benchmarks for restaurant quality and customer demand.

---

## Revenue Analysis

FoodHub earns revenue by collecting a margin on restaurant orders.

Based on the provided commission structure, the estimated net revenue generated from the analyzed dataset was:

**$6,166.30**

This demonstrates how order-level data can be translated into financial insights.

---

## Delivery Performance

Delivery time was analyzed across different order patterns and days of the week.

Approximately **10.54% of orders took more than 60 minutes** from preparation through delivery.

Weekday delivery times were higher than weekend delivery times, highlighting a potential operational bottleneck during weekday periods.

---

## Weekday vs. Weekend Demand

Order demand differs substantially across weekdays and weekends.

Approximately **71% of total orders were placed on weekends**.

This concentration of demand has important implications for:

- Delivery staffing
- Restaurant preparation capacity
- Inventory planning
- Promotional timing
- Resource allocation

---

# Key Business Insights

## 1. Weekend Demand Dominates Order Volume

Approximately **71% of FoodHub orders occur on weekends**.

### Business Implication

FoodHub should treat weekends as its primary demand period and align operational resources accordingly.

---

## 2. Weekday Delivery Efficiency Is an Opportunity

Weekday deliveries take longer than weekend deliveries.

### Business Implication

FoodHub should investigate traffic, driver availability, and delivery-zone inefficiencies during weekday peak periods.

---

## 3. Customer Feedback Coverage Is Incomplete

Nearly **40% of orders are unrated**.

### Business Implication

Incomplete rating data limits FoodHub's ability to accurately assess:

- Restaurant quality
- Customer satisfaction
- Delivery experience
- Service gaps

---

## 4. Popular Cuisines Can Drive Marketing Strategy

American, Japanese, and Italian cuisines combine strong demand with favorable ratings.

### Business Implication

These cuisines can be prominently featured in high-volume marketing campaigns.

Premium cuisines such as French, Thai, and Spanish can be positioned as higher-value or special-experience options.

---

## 5. High-Performing Restaurants Can Serve as Benchmarks

Restaurants such as Shake Shack and Blue Ribbon Sushi Izakaya demonstrate strong performance.

### Business Implication

FoodHub can use high-performing partners as benchmarks for:

- Service quality
- Customer satisfaction
- Delivery readiness
- Restaurant operating practices

---

## 6. Customer Spending Behavior Enables Segmentation

Order-value differences create opportunities to distinguish between:

- High-spend customers
- Price-sensitive customers

### Business Implication

FoodHub can tailor promotions and recommendations to customer value segments.

---

## 7. Historical Demand Can Support Resource Planning

Strong weekend concentration and delivery-time patterns can be used to guide staffing and supply decisions.

### Business Implication

Demand analysis can improve:

- Driver allocation
- Restaurant staffing
- Delivery capacity
- Inventory planning

---

# Business Recommendations

## Recommendation 1 — Improve Weekday Delivery Efficiency

Weekday delivery performance should be a priority.

FoodHub can:

- Improve route optimization
- Increase driver allocation during weekday lunch and evening peaks
- Use real-time traffic information
- Identify frequently delayed delivery zones
- Improve driver-to-order matching

This can help reduce delivery delays and improve customer experience.

---

## Recommendation 2 — Encourage More Customer Ratings

With nearly 40% of orders unrated, FoodHub should increase customer participation in post-delivery feedback.

Potential actions include:

- Loyalty points for leaving ratings
- Small promotional incentives
- Simplified rating flows
- Post-delivery reminders
- In-app prompts

Better rating coverage would improve FoodHub's ability to evaluate restaurant and delivery performance.

---

## Recommendation 3 — Promote High-Rated and Popular Cuisines

American, Japanese, and Italian cuisines should be featured prominently in high-volume campaigns.

FoodHub can also position cuisines such as French, Thai, and Spanish as premium or special-experience offerings.

This supports both:

- High-demand customer acquisition
- Higher-value order opportunities

---

## Recommendation 4 — Benchmark Restaurant Performance

FoodHub should evaluate restaurants using a structured combination of:

- Order volume
- Ratings
- Delivery performance
- Customer demand

Restaurants can be grouped into segments such as:

```text
High Performer
Improvement Needed
Low Demand
```

High-performing restaurants can be used as benchmarks.

Restaurants needing improvement can receive:

- Operational guidance
- Service-quality training
- Targeted promotions
- Personalized support

---

## Recommendation 5 — Introduce Performance-Based Incentives

FoodHub can explore dynamic commission or incentive structures for restaurants.

For example, restaurants that maintain:

- Strong ratings
- High order volume
- Fast preparation times
- Reliable service

could receive preferential incentives or lower commissions.

This can encourage restaurants to prioritize both quality and operational efficiency.

---

## Recommendation 6 — Segment Customers for Personalized Marketing

FoodHub can segment customers based on spending behavior.

### High-Spend Customers

Recommend:

- Premium cuisines
- New restaurant experiences
- Higher-value meal options
- Loyalty offers

### Price-Sensitive Customers

Recommend:

- Budget-friendly restaurants
- Discounts
- Value meals
- Reliable lower-cost options

This can improve both customer relevance and marketing effectiveness.

---

## Recommendation 7 — Use Association Analysis for Better Recommendations

FoodHub can analyze ordering patterns to identify relationships such as:

```text
Customers who ordered X
      ↓
Often also order Y
```

Association-rule techniques can support:

- Cross-selling
- Personalized restaurant recommendations
- Cuisine recommendations
- Bundled promotions

---

## Recommendation 8 — Use Demand Forecasting for Operations

Because approximately **71% of orders occur on weekends**, FoodHub can use historical demand patterns to improve operational planning.

Potential applications include:

- Driver scheduling
- Restaurant staffing
- Delivery capacity
- Inventory preparation
- Peak-period planning

This can improve resource utilization and reduce service bottlenecks.

---

# Strategic Opportunities

The analysis suggests several areas where FoodHub can extend its use of data.

## Restaurant Segmentation

Restaurants can be grouped based on:

- Ratings
- Order volume
- Delivery performance
- Revenue contribution

This can help FoodHub differentiate between strategic partners and restaurants needing operational support.

---

## Predictive Revenue Modeling

A future predictive model could estimate how changes in:

- Commission rates
- Promotions
- Pricing
- Restaurant performance

may affect FoodHub's revenue.

This would support more informed commercial decisions.

---

## Customer Recommendation Systems

Customer ordering history can support:

- Cuisine recommendations
- Restaurant recommendations
- Personalized offers
- Cross-selling

This can increase customer engagement and repeat ordering.

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

A key data-quality issue was identified in the rating column, where **736 orders were recorded as `"Not given"`**, representing nearly 40% of orders.

Approximately **71% of total orders occur on weekends**, making weekend demand a major operational planning factor.

The analysis also found that approximately **10.54% of orders exceeded 60 minutes**, while weekday delivery times were higher than weekend delivery times.

Using the provided commission rules, FoodHub's estimated revenue from the analyzed orders was approximately **$6,166.30**.

The findings suggest several actionable opportunities, including:

- Improving weekday delivery efficiency
- Increasing customer rating participation
- Promoting popular and high-rated cuisines
- Benchmarking restaurant performance
- Introducing performance-based restaurant incentives
- Segmenting customers for personalized marketing
- Using association analysis for recommendations
- Applying demand forecasting for staffing and resource planning

Overall, the project demonstrates how exploratory data analysis can convert transactional food-delivery data into practical insights across operations, marketing, restaurant partnerships, customer engagement, and revenue strategy.

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
- Customer Segmentation Concepts
- Restaurant Segmentation Concepts
- Demand Planning
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

This project demonstrates how **Exploratory Data Analysis can transform transactional food-delivery data into actionable business insights**.

The strongest opportunities identified are improving weekday delivery performance