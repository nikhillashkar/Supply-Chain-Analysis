# AI Workflow Documentation

This document contains representative AI prompts and explanations related to the Supply Chain Analysis project. It describes how AI can help explain the dataset, analytical logic, and business insights.

## Stage 1: Understanding the Dataset

### Q1. What information does this dataset contain?

**Answer:**

The dataset contains information about customer orders, products, sales, profit, shipping, and delivery performance.

### Q2. What is the purpose of `df.head()` and `df.info()`?

**Answer:**

`df.head()` displays the first five rows of the dataset. `df.info()` provides information about the number of rows and columns, data types, and non-null values.

### Q3. Which columns are important for delivery performance analysis?

**Answer:**

Important columns include `Days for shipping (real)`, `Days for shipment (scheduled)`, `Delivery Status`, `Late_delivery_risk`, `Shipping Mode`, and `Order Region`.

### Q4. Why is it important to check missing values?

**Answer:**

Checking missing values helps identify incomplete data. For example, `Order Zipcode` contains many missing values, and `Product Description` is entirely empty in this dataset. These columns should be evaluated before deciding how to handle them.

## Stage 2: Data Cleaning and Analysis

### Q1. Why is data cleaning important before analysis?

**Answer:**

Data cleaning helps identify missing values, duplicate records, and incorrect data types. It improves data quality and makes the analysis more reliable.

### Q2. How can actual shipping days be compared with scheduled shipping days?

**Answer:**

We can compare `Days for shipping (real)` with `Days for shipment (scheduled)`. If actual shipping days are greater than scheduled shipping days, the order took longer than planned.

### Q3. How can order profitability be analyzed?

**Answer:**

We can use `Order Profit Per Order` to classify orders as profitable, loss-making, or break-even. This helps us understand the profitability distribution.

### Q4. How can delivery bottlenecks be identified?

**Answer:**

We can compare delivery delay percentages across shipping modes, regions, customer segments, departments, and order statuses. This helps identify areas that may need further investigation.

## Stage 3: Insights and Visualization

### Q1. Why are visualizations useful in delivery performance analysis?

**Answer:**

Visualizations help us compare delivery performance across different categories. They make patterns, differences, and potential bottlenecks easier to understand.

### Q2. Which shipping modes have the highest delivery delay percentages?

**Answer:**

According to the project report, First Class has a 100% delay rate, Second Class has 79.8%, Standard Class has 39.8%, and Same Day has 0%. These results highlight shipping mode as an important area for investigation.

### Q3. How does delivery delay analysis relate to profitability?

**Answer:**

The report estimates $2.1 million in profit at risk from delayed orders. Analyzing delivery performance alongside profitability helps identify potential business risks.

### Q4. How can time-based analysis help improve delivery performance?

**Answer:**

Analyzing delivery delays by month and hour helps identify periods with higher delay rates. The report identifies August and September at 55.4% and hour 21 at 57.1%, which can help guide further investigation and capacity planning.
