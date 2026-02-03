# Sales Performance Dashboard

## Business Problem
The business needs a centralized dashboard to monitor sales performance,
track growth trends, and compare regional and product-level results
for better decision-making.

## Data Overview
The dataset contains:
- Sales transactions
- Customer details
- Product information
- Date (calendar) table

## Key KPIs
- Total Sales
- Year-over-Year (YoY) Growth
- Month-over-Month (MoM) Growth
- Average Order Value
- Sales by Region
- Sales by Product Category

## Data Model
The report uses a star schema data model with:
- Fact table: Sales
- Dimension tables: Date, Product, Customer, Region

## Technical Highlights
- Star schema data modeling
- Advanced DAX measures
- Time intelligence calculations
- Drill-through and tooltips
- Optimized visuals for performance

## Sample DAX Measures

Total Sales =
SUM ( Sales[SalesAmount] )

YoY Sales =
CALCULATE (
    [Total Sales],
    SAMEPERIODLASTYEAR ( 'Date'[Date] )
)

YoY Growth % =
DIVIDE (
    [Total Sales] - [YoY Sales],
    [YoY Sales]
)
