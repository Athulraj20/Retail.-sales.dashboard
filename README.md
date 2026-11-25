Retail Sales Dashboard

An interactive Power BI portfolio project for exploring sales across six Bengaluru store IDs. The report helps answer when sales changed, which products contributed, and which transactions explain the change.

## Report pages

| Page | Business question |
| --- | --- |
| Overview | How are sales, orders, and units performing? |
| Trends | When did sales change, and how does the same period compare with last year? |
| Customers | Which customer groups contribute to sales? |
| Products | Which products and categories lead by sales or units? |
| Customer Info | Which transactions explain an individual customer’s activity? |
| Product Info | How does an individual product perform over time? |

Built with **Power BI Desktop, Power Query, and DAX**. The report uses custom visuals alongside standard report visuals.

## Data model and preparation

- `Orders` provides order-level records. `Order_Items` provides line-level records for product sales and quantities.
- Order keys connect orders to line items. A calendar supports period filtering and prior-year comparisons, while store IDs identify the six store zones.
- Power Query was used to investigate order dates that appeared in the wrong month and compare them with corrected dates using the order lookup.

## KPI definitions

| Metric | Definition |
| --- | --- |
| Product Sales | Sales value from order lines |
| Total Orders | Distinct order keys in the selected context |
| Total Units | Sum of item quantities |
| Average Selling Price | Product Sales divided by Total Units |
| Sales YoY % | Change in sales divided by prior-year sales for the comparable period |
| Estimated Profit | Product Sales multiplied by the assumed margin |
| Estimated COGS | Product Sales less Estimated Profit |

Actual product costs were unavailable. The project uses assumed margins of **17.5% for the current-year estimate** and **15% for the prior-year estimate**. These percentages are inputs to a scenario. Compare partial years with the same date range in the prior year. Customer analysis uses names where stable customer IDs were unavailable. Delivery timing is based on store rules.

## Portfolio data

Original customer names were replaced with fictional names in selected records during preparation for this portfolio project. Fictional names serve as display labels. Buyer counts and repeat-buyer comparisons based on those labels are approximate.

## Open the report

1. Download `Retail Dashboard.pbix` from the repository.
2. Open it in **Power BI Desktop** on Windows to explore the report and its slicers.
3. For refresh or reproduction, use a shareable source with matching tables and columns. In Power BI Desktop, update the source location under **Transform data → Data source settings**, then refresh.
