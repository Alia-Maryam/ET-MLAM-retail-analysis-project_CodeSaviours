# ET-MLAM-retail-analysis-project_CodeSaviours
Retail Sales Performance Analysis

A portfolio-ready retail data analysis project using Python, Pandas, NumPy, and Matplotlib to understand sales performance, profitability, discounting, regional efficiency, and customer segments.

📌 Project Overview

This project simulates the work of a Data Analyst at a national retail chain ("Superstore").

Business Problem

Leadership wants to know: where are we making money, where are we losing it, and what should we change in our discounting and regional strategy to improve profitability?

The notebook follows an end-to-end analytics workflow:

Business question → Data loading → Data quality checks → Feature engineering → EDA → KPI analysis → Visualization → Deeper analysis → Business recommendations

🎯 Objectives

The analysis aims to answer five core business questions:

Is the business growing over time?

Which product categories generate the most sales and profit?

Which sub-categories are losing money?

How does performance differ across regions?

Which customer segments contribute most to profitability?

A deeper analysis also investigates:

Whether heavy discounting reduces profit margins

Whether shipping speed is associated with profitability

Where Furniture losses are concentrated in the Central region

🗂️ Dataset

The notebook uses the superstore.csv retail dataset.

The executed notebook contains:

10,800 rows

21 columns

Order-level transaction data

Order and shipping dates

Customer information

Product categories and sub-categories

Sales, quantity, discount, and profit

Region and customer segment

Shipping mode

Key fields include:

Column

Description

Order ID

Unique order identifier

Order Date

Date the order was placed

Ship Date

Date the order was shipped

Ship Mode

Shipping method

Customer ID

Customer identifier

Segment

Customer segment

Region

Sales region

Category

Product category

Sub-Category

Product sub-category

Sales

Sales revenue

Quantity

Quantity purchased

Discount

Discount applied

Profit

Profit generated

🛠️ Technologies Used

Python

Pandas — data loading, cleaning, transformation, grouping, and aggregation

NumPy — numerical calculations and correlation analysis

Matplotlib — business visualizations

Jupyter Notebook — analysis environment

🔍 Analysis Workflow

1. Data Loading

The notebook loads superstore.csv using Pandas and performs an initial inspection of:

Dataset dimensions

Column names

Data types

Sample records

2. Data Quality Checks

The notebook checks for:

Missing values

Duplicate rows

Date validity

Negative Sales

Negative Quantity

Zero Sales

The executed notebook output reports:

806 missing values across several fields

504 duplicate rows

No negative Sales

No negative Quantity

No zero Sales

Note: The notebook's explanatory markdown describes the dataset as clean, but the executed output actually identifies missing values and duplicates. The README reflects the executed results.

3. Feature Engineering

Several analytical variables are created:

Order Year

Order Month

Order Year-Month

Profit Margin

Shipping Days

Is_Loss

Sales_Category

Discount Bucket

The Sales_Category variable groups transactions into:

Small — Sales < $50

Medium — $50–$500

Large — Sales > $500

📊 Key Performance Indicators

The notebook calculates the following KPIs:

KPI

Result

Total Sales

$2,297,200.86

Total Profit

$286,397.02

Overall Profit Margin

12.47%

Average Discount

15.62%

Unique Orders

5,015

Average Order Value

$458.07

The analysis also identifies 1,871 loss-making transactions, representing 17.3% of the transactions in the executed dataset.

📈 Visual Analysis

The notebook contains visualizations designed around specific business questions.

Sales Trend

Monthly sales are analyzed across the available period, with the notebook highlighting a recurring sales increase toward the end of the year.

Category Performance

Sales and profit are compared across:

Technology

Furniture

Office Supplies

Executed results:

Category

Sales

Profit

Technology

$836,154.03

$145,454.95

Furniture

$741,999.80

$18,451.27

Office Supplies

$719,047.03

$122,490.80

Sub-Category Profitability

Three sub-categories show overall negative profit:

Sub-Category

Profit

Tables

-$17,725.48

Bookcases

-$3,472.56

Supplies

-$1,189.10

Regional Performance

Region

Sales

Profit

Margin

West

$725,457.82

$108,418.45

14.9%

East

$678,781.24

$91,522.78

13.5%

South

$391,721.91

$46,749.43

11.9%

Central

$501,239.89

$39,706.36

7.9%

The notebook emphasizes comparing profit margin, not only sales volume, when evaluating regional efficiency.

Customer Segments

The notebook compares:

Consumer

Corporate

Home Office

using total sales, total profit, order count, and average discount.

💸 Discount vs. Profitability

One of the main analyses investigates whether higher discounts are associated with lower profit margins.

The notebook groups transactions into discount buckets:

Discount Level

Average Profit Margin

No Discount

34.0%

1–20%

17.4%

21–40%

-16.7%

41–60%

-63.4%

60%+

-122.5%

The notebook's analysis concludes that average transaction profitability becomes negative once discounts move beyond roughly 40%.

Important note

The notebook also calculates a correlation between Discount and Profit Margin, but the executed output returns NaN. Therefore, the bucket-level results are the meaningful quantified evidence presented in the notebook rather than a usable correlation coefficient.

🚚 Shipping Analysis

Shipping performance is compared across:

Same Day

First Class

Second Class

Standard Class

The notebook calculates total sales, total profit, average shipping days, and average profit per order.

The analysis concludes that faster shipping does not show a clear, consistent relationship with higher profit per order in this dataset.

🔎 Final Deep Dive: Furniture in the Central Region

The final analysis narrows the investigation to Furniture sales in the Central region.

Results:

481 Furniture transactions

$163,797.16 in Sales

-$2,871.05 in Profit

-1.75% Profit Margin

Profit by Furniture sub-category:

Sub-Category

Profit

Furnishings

-$3,906.22

Tables

-$3,559.65

Bookcases

-$1,997.90

Chairs

$6,592.72

This deeper analysis shows that the Furniture problem is not evenly distributed: some sub-categories are profitable while others generate losses.

💡 Main Business Findings

The notebook highlights five major findings:

Sales show strong seasonality, with higher activity toward the end of the year.

Technology is the largest sales and profit contributor among the three product categories.

Several specific sub-categories lose money overall, particularly Tables, Bookcases, and Supplies.

Deep discounting is associated with negative average profit margins, with average profitability turning negative above roughly 40% discount.

Regional performance differs in efficiency, making profit margin an important KPI alongside sales.

The final Furniture/Central deep dive further shows that loss-making sub-categories can be identified without treating the entire Furniture category as unprofitable.

📌 Business Recommendations Presented in the Notebook

The notebook proposes:

Planning inventory and staffing around seasonal demand.

Investigating Furniture pricing and cost structure.

Reviewing supplier costs and discount policies for loss-making sub-categories.

Setting tighter controls around deep discounts.

Tracking regional Profit Margin alongside Sales.

Targeting specific loss-making Furniture sub-categories rather than applying blanket restrictions.

These recommendations are based on the analyses performed in the notebook.

📁 Project Structure

A simple GitHub repository can be organized as:

retail-sales-analysis/
│
├── retail_analysis_project_solved.ipynb
├── superstore.csv
├── README.md
└── requirements.txt

requirements.txt

pandas
numpy
matplotlib
jupyter

▶️ How to Run the Project

1. Clone the repository

git clone <your-repository-url>
cd retail-sales-analysis

2. Install dependencies

pip install -r requirements.txt

3. Launch Jupyter Notebook

jupyter notebook

4. Open the notebook

Open:

retail_analysis_project_solved.ipynb

Make sure superstore.csv is located in the same directory as the notebook.

📚 Skills Demonstrated

This project demonstrates practical data analyst skills including:

Data loading and inspection

Data quality validation

Missing-value and duplicate detection

Date transformation

Feature engineering

Pandas groupby and aggregation

KPI development

Exploratory Data Analysis

Business-oriented visualization

Profitability analysis

Discount analysis

Regional analysis

Customer segmentation analysis

Translating analytical results into business recommendations

🚀 Possible Future Improvements

The notebook suggests several ways to extend the project:

Time-series forecasting — predict future sales using a moving average or statsmodels.

RFM customer segmentation — segment customers using Recency, Frequency, and Monetary value.

Regression modeling — predict Profit using Sales, Discount, and Category with scikit-learn.

Interactive dashboard — recreate the analysis using Plotly or Streamlit.

Portfolio publication — publish the notebook and a short business-focused project summary.

👤 Portfolio / CV Description

You can describe the project on a CV as:

Retail Sales Performance Analysis — Analyzed 10,800 retail transactions using Python, Pandas, NumPy, and Matplotlib. Built business KPIs, performed data quality checks and feature engineering, analyzed regional and product profitability, and investigated the relationship between discounting and profit margins. Identified loss-making product sub-categories and developed data-backed business recommendations.

📄 Project Status

Completed: End-to-end exploratory retail sales and profitability analysis.

Primary tools: Python · Pandas · NumPy · Matplotlib · Jupyter Notebook
