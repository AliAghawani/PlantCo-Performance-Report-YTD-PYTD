# PlantCo Performance Report – YTD / PYTD ⭐

## Project Overview 📝
📊 Developed as part of my ongoing **Power BI & DAX mastery journey**.  
A single-page interactive dashboard that helps PlantCo’s leadership:

- **Track 3 Core KPIs**: **Sales, Gross Profit, Quantity**.  
- **Compare YTD vs PYTD** even when the current year is incomplete (data through 14 Apr 2024).  
- **Pinpoint Pain Points & Growth Areas** across month ⇄ country ⇄ product with one slicer.

## Data Preparation & Modeling
- **Dim_Date** calendar (2022-2024) with `InPast` flag to avoid blanks in PYTD.  
- **Power Query**: typed columns, removed nulls, aligned date keys.  
- **Star Schema**: `Fact_Sales` + dimension tables (Date, Account, Product).

## DAX Highlights 🔥
| Purpose | Measure / Logic |
|---------|-----------------|
| **Base KPIs** | `Sales`, `Quantity`, `Gross Profit` (`Sales – COGS`) |
| **Time Intel** | `TOTALYTD`, `SAMEPERIODLASTYEAR` with `Dim_Date[InPast]` |
| **Dynamic Switch** | `SWITCH()` + `SELECTEDVALUE()` → one slicer drives every visual |
| **Adaptive Titles** | Report & visual headers change with KPI and year selection |

## Report Structure 📈
1. **Dynamic Header**: “PlantCo *<KPI>* Performance *<Year>*”.
2. **Slicers**  
   - **Date Slicer**
   - **KPI Slicer**: KPI Slicer: Sales · Gross Profit · Quantity (drives the entire page).
3. **Treemap**: Bottom-10 YTD vs PYTD | Country.
4. **Waterfall**: *KPI* YTD vs PYTD by Month – Country – Product.  
5. **Column Chart**: *KPI* YTD & PYTD monthly comparison.  
6. **Scatter**: Profitability segmentation (GP % vs *KPI*).  
7. **Insights Cards**: KPI delta, GP %


## Key Insights 🚀
- **March & April 2024**: sharp **Gross Profit decline** driven mainly by **Canada › Landscape** segment.  
- **February 2024** outperformed prior-year-to-date across all KPIs — replicate winning tactics.  
- Concentrated revenue in few markets → **diversify** to stabilize profits.

## Technologies & Tools 🔧
- Microsoft **Power BI Desktop** (May 2024)  
- **DAX**: time-intelligence, switch measures, dynamic titles  
- **Power Query**, star-schema modeling  
- Interactive visuals: slicers, tooltips, drill-through

## Author 👤
**Ali Aghawani** 

[LinkedIn](https://www.linkedin.com/in/ali-aghawani) • aliaghawani215@gmail.com
