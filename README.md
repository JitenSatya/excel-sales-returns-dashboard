# Sales & Returns Dashboard (Excel)

![Dashboard](dashboard.png)
<img width="1371" height="817" alt="dashboard png" src="https://github.com/user-attachments/assets/aea0c403-eace-4f39-b22d-eabd9ae9c3a1" />


## Business problem
A sales director wants to know where revenue is strongest, how much is lost to returns, and whether discounts and promotions help.

## Dataset
Product-Sales-Region: 1,500 orders (Jan 2023 to Jun 2025), 19 columns. Dataset - [Sample Sales Data Excel Download – 5 Free Datasets | Excelx.com](https://excelx.com/practice-data/sales-retail/)

## Questions
1. Which regions and products drive gross vs net revenue?
2. Where do returns hurt most?
3. Do discounts and promotions change order size or returns?

## KPI definitions
- Gross Revenue = sum of TotalPrice (4.38M)
- Net Revenue = TotalPrice excluding returned orders (3.27M)
- Revenue Lost = TotalPrice of returned orders (1.11M, 25.3% of gross)
- Return Rate = share of orders returned (24.8%)
- Average Order Value = 2,920

## What I did
- Kept the raw sheet and worked on a copy as an Excel Table
- Filled blank Promotion cells with "NONE"; removed duplicate Date column
- Added NetRevenue, ReturnedRevenue, ReturnStatus, DeliveryDays, Year, Quarter
- Built pivot tables, combo charts, and slicers (Region, Product, CustomerType)

## Key insights
1. Returns are a major revenue leak. 25.3% of gross revenue (1.11M of 4.38M) came from returned orders, leaving 3.27M in net revenue.
2. West and Laptop lose the most. West loses 261K, the most of any region, and falls from 3rd on gross to last on net. Laptop loses 213K, the most of any product, while Chair has the highest return rate (28.2%).
3. Discounts of 10–15% lowered order value (2,845 and 2,686, vs 3,067 with no discount) without raising order quantity (about 10.2–10.6 units at every level).
4. Promotions show little effect. Return rates stay within 23.9%–26.0% across promotion types.


## Recommendation
- Investigate returns in West, Laptops, and Chairs first. The dataset has no return reasons, so start collecting them (quality, shipping, wrong item) to find the real cause.
- Review blanket 10–15% discounts. They lowered order value without raising quantity, so test targeted promotions instead.
- Report net revenue next to gross revenue in all sales reports, since about 25% of gross was returned.

## Limitations
- Data appears synthetic; the ~25% return rate is unusually high
- Promotion codes don't match the Discount column (e.g., SAVE10 orders have several discount levels)
- TotalPrice excludes ShippingCost
- Differences between groups are small and not statistically tested
- Currency units are not specified in the dataset

## Tools
Excel (Tables, PivotTables, PivotCharts, slicers)

# Download the workbook
[Sales_Returns_Dashboard.xlsx](https://github.com/user-attachments/files/35032155/Sales_Returns_Dashboard.xlsx)
Open in Excel to use the slicers
