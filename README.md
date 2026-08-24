# Quantium Retail Analytics: Customer Insights & Store Trial Performance Analysis
### Executive Summary
This repository contains an end-to-end data analytics project evaluated on transaction and customer behavior data for Quantium. The analysis is divided into two primary phases:
 * Task 1: Transaction Data Cleaning & Customer Segmentation: Data preprocessing, string parsing, memory optimization, and exploratory data analysis across customer lifestages and purchasing behaviors.
 * Task 2: Store Trial & Control Matching Analysis: Identifying suitable benchmark control stores using statistical similarity metrics (Pearson correlation + Min-Max distance) to measure sales uplift during a 5-month store layout trial.
Dataset Overview
The analysis utilizes FMCG transaction logs merged with demographic profiles:
 * Total Transactions: 264,834 records
 * Timeframe: July 2018 – June 2019
 * Features: Loyalty Card ID, Store Number, Transaction ID, Product Name, Pack Size, Brand, Customer Lifestage, and Premium Segment.
Key Technical Highlights
1. Data Cleaning & Memory Optimization
 * Extracted numerical PACK_SIZE (g) and normalized BRAND categories from unstructured string product names.
 * Optimized data types (downcasting integers, converting strings to categorical data types), reducing memory footprint by 50.8% (from 24.2\text{ MB} \rightarrow 11.9\text{ MB}).
2. Control Store Selection Methodology (Task 2)
Control stores were matched to Trial Stores (77, 86, and 88) using pre-trial historical data (July 2018 – January 2019). Similarity was calculated using a weighted composite score:
 * Trial Store 77 \rightarrow Matched with Control Store 233
 * Trial Store 86 \rightarrow Matched with Control Store 155
 * Trial Store 88 \rightarrow Matched with Control Store 237
Key Business Results & Trial Impact
+-------------+-----------------+-------------------------+-----------------------------------------------------+
| Trial Store | Matched Control | Avg Monthly Revenue Lift| Key Growth Driver                                   |
+-------------+-----------------+-------------------------+-----------------------------------------------------+
| Store 77    | Store 233       | +21.6%                  | Significant surge in unique customer visits (+20%)  |
| Store 86    | Store 155       | +8.4%                   | Moderate increase in transaction volume             |
| Store 88    | Store 237       | +13.2%                  | Sustained increase in traffic & total units sold    |
+-------------+-----------------+-------------------------+-----------------------------------------------------+

 * Footfall Expansion: Across all trial stores, revenue growth was primarily driven by an increase in unique customer traffic rather than spend per transaction.
 * Store Layout Success: Trial Store 77 and Trial Store 88 demonstrated consistent, positive lift across key performance metrics throughout the 5-month trial period.
Tech Stack & Libraries
 * Language: Python 3.x
 * Data Wrangling: Pandas, NumPy
 * Statistical Analysis: SciPy (scipy.stats)
 * Data Visualization: Matplotlib, Seaborn
Business Recommendation
 * Roll Out Store Layout: Expand the trial layout across similar high-footfall regional stores, as it provenly increases customer acquisition and foot traffic.
 * Operational Check on Store 86: Investigate Store 86's implementation details to ensure layout changes strictly adhered to trial guidelines, given its moderate lift relative to Stores 77 and 88.
