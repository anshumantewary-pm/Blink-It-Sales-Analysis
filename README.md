# Blinkit Grocery Sales Analysis

An Excel-based exploration of item-level sales data from Blinkit, the Indian quick-commerce grocery platform. The workbook turns the raw sales records into a structured Excel table, then charts how sales and product visibility are distributed. The aim is to understand which product attributes and outlet characteristics drive revenue across stores.

## Dataset

File: [`BlinkIT Grocery Data.xlsx`](BlinkIT%20Grocery%20Data.xlsx), sheet `BlinkIT Grocery Data` (Excel table `Table1`)

- **8,523 rows**, one per item-outlet sales record
- **1,559 unique items** across **10 outlets** (outlets established between 2011 and 2022)
- **16 item categories**, e.g. Fruits and Vegetables, Snack Foods, Household, Frozen Foods and Dairy

| Field | Description |
|---|---|
| `Item Fat Content` | Low Fat / Regular |
| `Item Identifier` | Product code |
| `Item Type` | Product category |
| `Outlet Establishment Year` | Year the outlet opened |
| `Outlet Identifier` | Outlet code |
| `Outlet Location Type` | Tier 1 / Tier 2 / Tier 3 |
| `Outlet Size` | Small / Medium / High |
| `Outlet Type` | Grocery Store, Supermarket Type1/2/3 |
| `Item Visibility` | Share of display area given to the item |
| `Item Weight` | Item weight |
| `Sales` | Sales value of the item at that outlet |
| `Rating` | Customer rating |

**Data-quality notes found in the raw data:**

- `Item Fat Content` uses inconsistent labels: `Low Fat`, `LF` and `low fat` mean the same thing, as do `Regular` and `reg`. These need to be standardised before grouping.
- `Item Weight` is blank in 1,463 rows.

## Approach

1. **Structuring.** Converted the raw range into an Excel table so it can be filtered, sorted and used in formulas.
2. **Distribution analysis.** Two charts are built into the sheet:
   - a **Pareto chart of `Sales`**, a histogram with a cumulative % line, showing how sales value is concentrated
   - a **scatter plot of `Item Visibility`** across all records, showing how display share is spread and flagging zero or outlier values
3. **Segmentation dimensions.** The data supports cuts by item category, fat content, outlet type, size, location tier and establishment year, for KPIs such as total sales, average sales, item count and average rating.

## What the Analysis Covers

- How sales are spread across items, and whether a small share of records drives most revenue (the Pareto view)
- How product visibility on shelves varies, and data issues such as zero-visibility items
- Outlet and product attributes that can be used for dashboard-style KPI breakdowns
- Data-cleaning steps needed before reporting

## Tools & Tech

- Microsoft Excel (Excel tables, filtering, Pareto/histogram and scatter charts, conditional formatting)

## Repository Structure

```
.
├── BlinkIT Grocery Data.xlsx   # Sales dataset with analysis charts
└── README.md
```

## How to Open

1. Clone the repository:
   ```bash
   git clone https://github.com/anshumantewary-pm/Blink-It-Sales-Analysis.git
   ```
2. Open `BlinkIT Grocery Data.xlsx` in Microsoft Excel 2016 or later. The Pareto chart needs a recent version of Excel.
3. Use the table filters to slice the data by outlet or item attributes. The charts sit beside the table.

---

**Author:** Anshuman Tewary · [GitHub](https://github.com/anshumantewary-pm) · [LinkedIn](https://www.linkedin.com/in/tewary-anshuman/)
