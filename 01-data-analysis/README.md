# Food Delivery Demand Analysis: Exploratory Data Analysis in Python

*Program project: FoodHub · Originally completed February 26, 2025*

**Executive summary:** A food delivery platform wanted to understand demand
across restaurants and cuisines to improve customer experience. Analyzing
~1,900 orders showed that demand is highly concentrated (5 of 14 cuisines
drive 87% of orders), weekday deliveries run 26% slower than weekends, and
39% of orders go unrated. The most important findings were gaps in the data
itself, which led to concrete instrumentation recommendations.

## Business problem
The company earns a margin on every order and wants to grow order volume and
customer satisfaction. Leadership needed a clear picture of what customers
order, when, how fast it arrives, and how they rate the experience.

## Approach
- Data: 1,898 orders from 1,200 customers across 178 restaurants
- Data quality review: identified non-standard missing values and implausible rating patterns
- Univariate and multivariate analysis of cuisine, cost, timing, and ratings
- Revenue modeling based on the company's tiered commission structure

## Key findings
- **Concentrated demand:** American, Japanese, Italian, Chinese, and Mexican cuisines account for 87% of orders.
- **Weekend-heavy business:** 71% of orders are placed on weekends.
- **Slower weekdays:** mean delivery is 28.3 minutes on weekdays vs. 22.5 on weekends.
- **Long end-to-end waits:** 10.5% of orders take over 60 minutes from order to door.
- **Low repeat rate:** 65% of customers ordered only once.
- **Satisfaction vs. feedback gap:** 84% of rated orders were 4–5 stars, but 39% of orders had no rating, and no orders were rated 1 or 2.
- **Independent drivers:** order cost, preparation time, and delivery time are essentially uncorrelated.

![Orders by cuisine type](images/orders-by-cuisine.png)

![Delivery time: weekdays vs. weekends](images/delivery-time-weekday-vs-weekend.png)

## Recommendations
1. **Fix the measurement gaps first:** split "preparation time" into cooking time and driver wait time, and capture the actual day and date of each order.
2. **Grow feedback coverage:** add lightweight rating prompts or incentives, and investigate why no low ratings appear.
3. **Grow weekday demand:** use day-specific promotions once day-level data is available.
4. **Diversify demand:** feature restaurants from under-ordered cuisines in the app.
5. **Speed up delivery at peak:** add driver incentives for high-demand periods.

## Data
1,898 anonymized food delivery orders, included in the [`data`](data/) folder. To run the notebook, place `foodhub_order.csv` in the same folder as the notebook.

## Skills & tools
Python, pandas, NumPy, Matplotlib, Seaborn · exploratory data analysis · data quality assessment · univariate & multivariate analysis · business recommendations
