# Financial Impact of Drought on California Almonds - A Power BI Analysis

> A comprehensive Power BI dashboard that visualizes the financial risks posed by severe drought conditions to California's multi-billion dollar almond industry.

<img width="1173" height="661" alt="image" src="https://github.com/user-attachments/assets/bfb3d8ef-526e-48a0-8437-a3ac4895978c" />


## 🚀 Project Summary

This project analyzes the relationship between drought severity and the financial health of the almond production sector in California. Using official data from the USDA and the U.S. Drought Monitor, this dashboard provides a dynamic tool for stakeholders to assess climate risk, identify high-risk counties, and understand historical trends.

The goal is to translate raw climate and agricultural data into a clear, interactive, and actionable financial narrative.

## 📊 Key Questions Answered

1.  **What is the estimated financial value** of the almond industry in key California counties?
2.  How has **drought severity** in California evolved over the past decade?
3.  Which **high-revenue counties** are facing the most significant and prolonged drought risk?
4.  What is the **changing composition of drought intensity** (e.g., from Moderate to Exceptional) during peak drought years?

## 🛠️ Tools & Techniques

* **Power BI:** Used for data modeling, analysis, and visualization.
* **Power Query:** Utilized for data cleaning, transformation, and merging of the almond and drought datasets.
* **DAX (Data Analysis Expressions):** Employed to create calculated measures for advanced analytics, including:
    * Estimated Revenue modeling.
    * Dynamic card and title text.
    * Average drought severity calculations.
* **Data Modeling:** Established a relationship between the two datasets based on `County` and `Year` to enable cross-filtering and comprehensive analysis.

## 📝 Key DAX Measures

A few of the key DAX measures created to power the dashboard's logic and interactivity:

```dax
// Calculates the estimated revenue based on average yield and price assumptions.
Estimated Revenue = [Total Almond Acres] * 2500 * 2.50

// Calculates the average drought intensity based on the USDM Level ID.
Average Drought Severity = AVERAGE(drought[USDMLevelID])

// Dynamically displays the selected location in a KPI card.
Selected Location = SELECTEDVALUE(drought[County], "All of California")

// Creates a dynamic title that updates based on the slicer selection.
Dashboard Title = "Almond Revenue & Drought Analysis for " & SELECTEDVALUE(drought[County], "All of California")
```

## 🚀 How to View the Project

1.  **Download** the `Almond Drought Analysis.pbix` file from this repository.
2.  **Open** the file using **Power BI Desktop**.
3.  Interact with the slicers and visuals to explore the data.

*Note: You must have Power BI Desktop installed on your machine to view the interactive report.*
