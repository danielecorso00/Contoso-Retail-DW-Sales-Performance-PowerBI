# Contoso Retail – Sales & Profitability Dashboard

## Overview
This project is an interactive **Power BI** report built on the Contoso Retail dataset (~100,000 sales transactions). 

The goal was to create a clear, reliable reporting tool for management to track revenue, profit margins, and channel performance across different countries—eliminating the need for manual spreadsheet checks.

---

## Dashboard Structure

### 1. Executive Overview
Provides a quick snapshot of overall company performance:
* **Main KPIs:** Total Revenue (`$219.84M`), Total Net Margin (`$122.91M`), Margin % (`55.91%`), and Previous Year Revenue comparison.
* **Monthly Revenue Trend:** Tracks sales evolution over time to highlight seasonality and growth periods.
* **Channel & Country Mix:** Compares physical retail stores by country against the Online channel.
* **Filters:** Interactive slicers for `Year` and store `Status` (`Open`, `Closed`, `Restructured`), synced across both pages.

![Executive Overview](screenshots/executive_overview.png)

### 2. Product & Customer Analysis
Focuses on product profitability and customer demographics:
* **Category & Brand Matrix:** Breaks down Revenue, Net Margin, and Margin % by product category and individual brand.
* **Brand Ranking:** Ranks all brands by total sales volume.
* **Customer Segmentation:** Shows how revenue is distributed across customer gender and countries.

![Product & Customer Analysis](screenshots/product_customer_analysis.png)

---

## How the Data Was Prepared
To make sure the numbers in the dashboard are accurate and consistent, I structured the work in three steps:
1. **Data Cleaning (Power Query):** Checked all four tables (`Sales`, `Product`, `Customer`, `Store`) for formatting issues, standardized decimal formats, cleaned missing store statuses, and removed unnecessary columns.
2. **Data Modeling:** Connected the sales table to the product, customer, store, and calendar tables in a clean star schema so that filters work reliably across the entire report.
3. **Standardization:** Converted all transactions into **USD** using daily exchange rates and labeled incomplete customer/product records as `"Unregistered"` or `"Uncategorized"`, keeping 100% of total revenue accounted for without blank entries.

---

## Key Takeaways from the Data
* **Online leads all channels:** E-commerce generates **$86.29M (39.25% of total revenue)**, outperforming every individual physical country market (followed by the United States at **$67.83M**).
* **Computers drive both volume and margin:** `Computers` is the top-performing category (**$53.04M**), with a net margin of **57.35%** (above the company average of **55.91%**).
* **Opportunity in customer registration:** Around **26.09% ($57.35M)** of revenue comes from unregistered guest purchases, pointing to clear room for growth through loyalty or CRM initiatives.

---

## Files in this Repository
* `Contoso_Retail_DW_PowerBI_Project_Daniele_Corso` – Full Power BI Desktop file.
* `screenshots/` – High-resolution images of the two dashboard pages.
