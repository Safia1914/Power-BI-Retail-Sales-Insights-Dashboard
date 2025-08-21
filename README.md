# Power-BI-Retail-Sales-Insights-Dashboard

## **Project Overview**

This project is a **Retail Sales Dashboard** built in **Power BI Desktop** using a cleaned retail dataset (Superstore/Walmart Sales Dataset).
The dashboard provides actionable insights into **sales performance, product trends, regional revenue, and profitability**, allowing businesses to make data-driven decisions.

---

## **Key Features**

* **Total Sales KPI** – Displays overall sales revenue.
* **Total Quantity KPI** – Shows the total number of items sold.
* **Profit Margin KPI** – Calculates the estimated profit margin using assumed 30% profit from sales.
* **Sales Trend Analysis** – Line chart showing monthly sales trends.
* **Year Slicer** – Allows filtering data by year for dynamic analysis.
* **Regional Sales Map** – Visualizes sales across different regions/states.
* **Top Products & Categories** – Highlights best-selling products and categories.
* **Interactive Filters** – Users can slice and dice data using various fields (Category, Region, Year).
* **Professional Dashboard Layout** – Includes a title, organized KPIs, visuals, and a clean layout.

---

## **Dataset**

* Source: [Superstore Sales Dataset](https://www.kaggle.com/datasets/juhi1994/superstore) *(or Walmart Sales Dataset if used)*
* Columns used:

  * `Order Date` (used for trend analysis, Month-Year hierarchy, Year slicer)
  * `Sales`
  * `Quantity`
  * `Region`
  * `Category`
  * `Product Name`
* Data Cleaning Steps:

  * Converted `Order Date` to Date type.
  * Removed unnecessary columns (Postal Code, Customer ID, etc.).
  * Handled empty/null rows.
  * Created calculated columns for **Profit** (`Sales * 0.3`) and **Month-Year** for trend analysis.

---

## **Tools & Technologies**

* **Power BI Desktop** – For dashboard building and visualization.
* **DAX (Data Analysis Expressions)** – For calculating measures such as Total Sales, Profit, Profit Margin.
* **Data Modeling** – To organize tables and relationships for interactive filtering.

---

## **Key Measures (DAX)**

```DAX
Total Sales = SUM(train[Sales])

Total Quantity = SUM(train[Quantity])

Profit = SUMX(train, train[Sales] * 0.3)

Profit Margin = DIVIDE(SUMX(train, train[Sales] * 0.3), SUM(train[Sales]), 0)
```

---

## **Learning Outcomes**

* Learned **data cleaning and transformation** in Power BI using Power Query.
* Built **interactive dashboards** with slicers, filters, and KPIs.
* Created **DAX measures** for dynamic calculations.
* Learned to **visualize trends, seasonality, and regional sales** effectively.
* Prepared a **professional dashboard layout** suitable for business decision-making.

---

## **How to Use**

1. Open the `.pbix` file in **Power BI Desktop**.
2. Use the **Year slicer** to filter data by year.
3. Click on **Region or Category** in visuals to drill down for deeper insights.
4. Hover over charts to see detailed values.



---

## **Conclusion**

This dashboard provides a **clear, interactive view of retail sales performance** across products, regions, and time.
It’s suitable for **business presentations, CV/portfolio showcase, and internship projects**, demonstrating skills in **Power BI, data modeling, and DAX calculations**.

