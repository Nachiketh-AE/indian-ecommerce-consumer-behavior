# Indian E-Commerce Consumer Behavior: Quick-Commerce Delivery Analysis

Final project for DACSS 603 (UMass Amherst, Spring 2025).

This project looks at 100,000 orders from three Indian quick-commerce apps (Blinkit, Swiggy Instamart, and JioMart) to understand what drives customer satisfaction and whether order delays follow predictable patterns.

**[View the full report](https://nachiii-1705.github.io/indian-ecommerce-consumer-behavior/603_final_project%20(2).html)**

## Research Questions

**RQ1: What factors influence customer satisfaction on e-commerce delivery apps?**
We examine how delivery time and order value relate to service rating. The expectation is that longer deliveries lower ratings, while higher order values are linked to higher ratings.

**RQ2: Are there patterns to order delays, and can we predict them?**
We test whether delays are more common on certain platforms, at certain times, or for certain product categories.

## Data

[`ecommerce_data.csv`](ecommerce_data.csv): 100,000 orders, 11 columns, no missing values.

| Column | Description |
|---|---|
| Order ID / Customer ID | Unique order and customer identifiers |
| Platform | Blinkit, Swiggy Instamart, or JioMart (roughly a third each) |
| Order Date & Time | Time the order was placed |
| Delivery Time (Minutes) | 5 to 76 minutes, median 30 |
| Product Category | Dairy, Grocery, Snacks, Fruits & Vegetables, Beverages, Personal Care |
| Order Value (INR) | ₹50 to ₹2,000, median ₹481 |
| Customer Feedback | Short free-text review |
| Service Rating | 1 to 5, mean 3.24 |
| Delivery Delay | Yes / No (13.7% of orders delayed) |
| Refund Requested | Yes / No (45.8% of orders) |

## Analysis So Far

- Data structure checks and summary statistics
- Missing value check (none found)
- Pairwise scatterplots of delivery time, order value, and service rating
- Histograms and boxplots to check distributions and spot outliers

## Tools

R, Quarto, tidyverse, GGally

## Repository Structure

```
.
├── 603_final_project (2).html   # Rendered report
├── 603_final_project.qmd        # Quarto source
├── ecommerce_data.csv           # Order-level dataset
└── README.md
```

## Reproducing the Analysis

```r
install.packages(c("tidyverse", "GGally"))
```

```bash
quarto render 603_final_project.qmd
```

## Authors

Nachiket Kadkol and Niranjan Prakash
