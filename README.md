# Sales Metrics Report for KPI Measurement


## Project Overview:
This project involved creating a comprehensive Sales Metrics Report for a client who required a detailed analysis of their sales performance using Power BI. The report was designed to measure key performance indicators (KPIs) over a one-month period and to be used as a template for ongoing future sales dataset reports. The client's objective was to gain actionable insights from their sales data, which included visualizations and DAX measures to evaluate sales performance across various dimensions.

## Project Objectives:
- Develop a Power BI dashboard that effectively visualizes key sales metrics.
- Create DAX measures for calculating sales performance on a monthly, quarterly, and yearly basis.
- Implement time intelligence in the data model using a custom calendar table.
- Provide insights on the top 3 and bottom 3 performing products.
- Standardize sales amounts across different currencies using a conversion rate to EUR.

## Key DAX Measures Created:

Sales for the Current Month:
 <pre> Sales for the Current Month = 
CALCULATE(
    [Total Amount in EUR],
    DATESMTD('Calendar'[Date])
)  </pre>

Sales for the Current Quarter:
 <pre> Sales for the Current Quarter = 
CALCULATE(
    [Total Amount in EUR],
    DATESQTD('Calendar'[Date])
) </pre>

Total Sales MTD (Month-to-Date) vs Same Period Last Year (MTD LY):
 <pre> Total Sales MTD = 
CALCULATE(
    [Total Amount in EUR],
    DATESMTD('Calendar'[Date])
)

Total Sales MTD LY = 
CALCULATE(
    [Total Amount in EUR],
    SAMEPERIODLASTYEAR(DATESMTD('Calendar'[Date]))
) </pre>

Total Sales QTD (Quarter-to-Date) vs Same Period Last Year (QTD LY):
 <pre> Total Sales QTD = 
CALCULATE(
    [Total Amount in EUR],
    DATESQTD('Calendar'[Date])
)

Total Sales QTD LY = 
CALCULATE(
    [Total Amount in EUR],
    SAMEPERIODLASTYEAR(DATESQTD('Calendar'[Date]))
) </pre>

Total Sales YTD (Year-to-Date) vs Same Period Last Year (YTD LY):
 <pre> Total Sales YTD = 
CALCULATE(
    [Total Amount in EUR],
    DATESYTD('Calendar'[Date])
)

Total Sales YTD LY = 
CALCULATE(
    [Total Amount in EUR],
    SAMEPERIODLASTYEAR(DATESYTD('Calendar'[Date]))
) </pre>











