# Online Retail Customer Analytics

### R | dplyr | Data Wrangling | Exploratory Data Analysis | Customer Analytics | Retail Analytics

## Project Overview

Conducted an end-to-end analysis of 500K+ online retail transaction records to evaluate customer purchasing behavior, revenue performance, geographic trends, product performance, returns, data quality, and transaction patterns.

The project transforms raw transaction-level data into business-focused insights using R for data preparation, transformation, aggregation, exploratory analysis, and visualization.

## Business Objectives

The analysis was designed to:

- Evaluate transaction activity and revenue across geographic markets
- Identify high-activity and high-value customers
- Analyze purchasing patterns across weekdays, months, and hours
- Identify products contributing the highest revenue
- Evaluate cancellation and return behavior
- Assess missing customer information
- Analyze repeat-purchase behavior
- Identify low-activity periods for planned website maintenance

## Dataset

The analysis uses an online retail dataset containing **541,909 transaction records** from a UK-based online retailer.

The transactions cover the period from **December 2010 through December 2011** and include customers across multiple countries.

### Key Variables

- `InvoiceNo` – Unique transaction/invoice identifier
- `StockCode` – Product identifier
- `Description` – Product description
- `Quantity` – Number of units in the transaction
- `InvoiceDate` – Transaction date and time
- `UnitPrice` – Price per unit
- `CustomerID` – Customer identifier
- `Country` – Customer country

A derived variable, `TransactionValue`, was created to measure the monetary value of each transaction.

## Tools & Technologies

- **R** – Data analysis and statistical computing
- **dplyr** – Filtering, grouping, aggregation, and data transformation
- **ggplot2** – Data visualization
- **R Markdown** – Reproducible analysis and reporting
- **Descriptive Statistics** – Data exploration and pattern identification

## Data Preparation

The dataset was loaded and inspected to understand its structure, variable types, distributions, and missing values.

A transaction-level revenue metric was created using:

`TransactionValue = Quantity × UnitPrice`

The invoice timestamp was also transformed into separate analytical features including:

- Transaction date
- Day of the week
- Hour of the day
- Month

These transformations enabled geographic, temporal, customer, and revenue analysis.

## Geographic & Revenue Analysis

Transaction activity and transaction value were aggregated by country to evaluate the geographic distribution of the retailer's business.

The analysis found that the **United Kingdom accounted for approximately 91.4% of transaction records**, indicating that transaction activity was highly concentrated in the retailer's domestic market.

Country-level transaction value was also calculated to identify markets generating significant revenue.

## Customer Analysis

Customer-level aggregation was performed to evaluate customer activity and value.

The analysis identified:

- The customer with the highest number of transactions
- The customer generating the highest total transaction value
- The number of unique Customer ID values represented in the data
- Repeat-purchase behavior
- Missing Customer ID patterns across countries

The analysis returned **4,373 unique Customer ID values** in the original dataset.

## Product Performance Analysis

Transaction values were aggregated by product to identify the item generating the highest total revenue.

This analysis demonstrates how transaction-level retail data can be transformed into product-level performance insights that can support merchandising and sales analysis.

## Time-Based Analysis

Transaction activity was analyzed across multiple time dimensions:

- Day of the week
- Month of the year
- Individual transaction dates
- Hour of the day

The analysis also evaluated consecutive hourly transaction activity to identify a potential two-hour website maintenance period with lower customer activity.

## Returns & Cancellation Analysis

Negative quantity values were used to identify cancelled transactions.

Cancellation behavior was evaluated for the French customer market by comparing cancelled transactions with overall transaction activity.

This provided a simple measure of return/cancellation behavior within that market.

## Data Quality Analysis

Missing values were calculated across dataset variables to identify potential data-quality issues.

Customer ID records received additional analysis to determine how missing customer information was distributed across countries.

## Key Findings

- The dataset contains more than **541K transaction records** covering approximately one year of online retail activity.
- The **United Kingdom represented approximately 91.4% of transaction records**, showing a strong geographic concentration.
- Customer-level analysis distinguished the most frequently active customer from the customer generating the highest transaction value.
- Transaction activity varied across weekdays, months, and hours, providing insight into customer shopping patterns.
- Missing Customer ID records were quantified and evaluated across countries.
- Cancellation behavior was measured using transactions with negative quantities.
- Product-level aggregation identified the retailer's highest revenue-generating product.
- The analysis returned **4,373 unique Customer ID values**.
- Transaction timing was evaluated to identify a lower-activity window for planned website maintenance.

## Analytical Workflow

`Raw Transaction Data`

↓  

`Data Inspection & Cleaning`

↓  

`Feature Engineering`

↓  

`Exploratory Data Analysis`

↓  

`Customer & Revenue Analysis`

↓  

`Product & Geographic Analysis`

↓  

`Time & Return Analysis`

↓  

`Business Insights`

## Skills Demonstrated

`R` `dplyr` `ggplot2` `Data Wrangling` `EDA` `Data Transformation` `Descriptive Statistics` `Customer Analytics` `Revenue Analysis` `Retail Analytics` `Data Quality Analysis` `Data Visualization`

## Repository Structure

```text
online-retail-customer-analytics/
│
├── README.md
├── data/
│   └── Online_Retail.csv
├── analysis/
│   └── online_retail_analysis.Rmd
├── scripts/
│   └── retail_analysis.R
├── images/
│   └── project_visualizations
└── docs/
    └── project_report.pdf
