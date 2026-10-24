# Sales Analysis by Territory and Year (Excel Power Query + Power Pivot)

> A Power Pivot analysis of 33.9M in total due across 8 sales territories from 2011 to 2014. Canada and Northwest bring in about 56% of the total, and Canada leads in every year.

![Total due by sales territory](images/sales_by_territory.png)

## 🎯 Business Question

Where do sales come from, and how do they change over time? Specifically:

- Which sales territories generate the most revenue?
- Which territories lead each year?
- How did total sales change from year to year?
- How much of the total due is product value, tax and freight?

## 📁 Data

- **Source:** Sales orders data from a data analysis diploma assignment
- **Territories (8):** Canada, Northwest, France, United Kingdom, Germany, Australia, Southwest, Central
- **Years:** 2011 to 2014
- **Measures:** # Orders, # Order Details, Qty, Subtotal, Tax Amount, Freight, TotalDue

## 🛠️ Tools

Microsoft Excel: Power Query, Data Model (Power Pivot), PivotTables, slicer, PivotChart

## 🔄 Process

1. **Loaded the sales orders table with Power Query** and reshaped the measures into an Item / Value layout, so one field holds every measure.
2. **Added the data to the Excel Data Model** (Power Pivot) to use as the source for the PivotTables.
3. **Built two PivotTables:**
   - all seven measures by sales territory
   - total due by year and territory
4. **Added a slicer** on the measure name, so one PivotTable can switch between measures, and a **line chart** of total due by year and territory.
5. **Checked the totals:** the territory figures add up to the year totals (33,933,557), and they match the 33.93M in my [Power BI sales dashboard](https://github.com/maghawry17-web/PowerBI-Sales-Dashboard).

## 🔍 Key Findings

- **Canada and Northwest bring in 55.6% of total due.** Canada leads with 11,939,530 (35.2%), followed by Northwest with 6,940,169 (20.5%).
- **Four territories make up 85%.** Canada, Northwest, France (5,198,110) and the United Kingdom (4,826,207) lead. Central is almost empty, with 38,127 in total due (0.1%).
- **Canada is the top territory in every year from 2011 to 2014.**
- **More territories appear in the data over time.** Only Canada and Northwest have sales in 2011, four territories have sales in 2012, and all eight have sales from 2013.
- **2013 was the peak year** at 16,041,760 (47.3% of the total), which is 85.0% higher than 2012. 2014 fell 55.0% from 2013 to 7,221,784.
- **Product value makes up most of the total.** Tax is about 8.6% of total due and freight about 2.7%, so product value is roughly 89%.

![Total due by year](images/sales_by_year.png)

## ⚠️ Data Notes

- The PivotTables in the workbook show a 2015 row that repeats the 2011 values exactly (1,323,329 in Canada and 675,662 in Northwest), which raises the workbook's grand total to 35,932,548. This README leaves 2015 out, and the resulting 33.93M matches the Power BI dashboard.
- The order, quantity, tax and freight totals in the workbook are affected by the same duplication, so they are not used here.
- 2011 starts in May, so the 2012 growth compares against a partial year.
- The 2014 total may cover only part of the year. Check the order dates before treating the 2014 drop as a real decline.
- The workbook's currency is not stated, so values are shown as plain amounts.

## ✅ Recommendations

- **Protect and grow Canada and Northwest**, since they carry more than half of the revenue.
- **Review the smallest territories** (Southwest at 2.7% and Central at 0.1%) and decide whether to invest in them or focus elsewhere.
- **Check why 2014 fell** (incomplete data or real demand) before using the yearly trend for planning.
- **Fix the 2015 duplicate in the workbook** by filtering it out or correcting the date logic in the Data Model.

## 📂 Files

- `workbook/sales-territory-powerpivot.xlsx` – the Excel workbook with the Data Model, PivotTables, slicer and chart
- `images/` – charts used in this README

## 👤 Author

Mohamed EL Maghawry · [LinkedIn](https://www.linkedin.com/in/mohamed-el-maghawry-a60232b4) · maghawry.17@gmail.com
