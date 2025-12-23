
#  **Quality Check: Ensuring Data Reliability & Integrity**  

During the **ETL process**, we ensure that every column meets **specific parameters and standards** to create **well-structured, reliable, and insightful** tables for the next steps.  

We are using **Medallion Architecture (Bronze, Silver, and Gold layers)** to build this **modern data warehouse**. At each stage, **data quality checks** help us maintain:  
**Reliability** – Ensuring accurate and consistent data.  
**Efficiency** – Reducing errors and improving performance.  
**Data Integration** – Providing clean and structured data for analytics.  

🚫 **No Quality Checks on the Bronze Layer!**  
- Since the **Bronze layer** stores **raw, unprocessed** data from source systems, we do **not** alter it.  
- Data validation and transformation occur in the **Silver & Gold layers**.  

---
## Medallion Architecture & Quality Checks

[![Medallion Architecture with Quality Checks](docs/images/medallion_architecture_quality_checks.png)](docs/images/medallion_architecture_quality_checks.png)

---
## **Quality Checks for the Silver & Gold Layers**  

 **File Structure:**  
```
tests/
├──  quality_checks_silver_[crm_cust_info].sql         # Customer Information  
├──  quality_checks_silver_[crm_prd_info].sql          # Product Information  
├──  quality_checks_silver_[crm_sales_details].sql     # Sales Data  
├──  quality_checks_silver_[erp_source_tables].sql     # ERP Source Validation  
└──  quality_checks_gold.sql                           # Final Gold Layer Checks  
```

---

## **Silver Layer Quality Checks**  

🔹 **`crm_cust_info` (Customer Info) **  
   - Ensures that customer data (names, emails, phone numbers, etc.) is **accurate and complete**.  
   - Identifies **missing, duplicate, or inconsistent** records.  

🔹 **`crm_prd_info` (Product Info) **  
   - Validates product details such as **names, categories, and prices**.  
   - Ensures **product consistency** across CRM and ERP systems.  

🔹 **`crm_sales_details` (Sales Data) **  
   - Checks for **correct transaction amounts, timestamps, and missing values**.  
   - Ensures proper relationships between **customers, products, and sales**.  

🔹 **`erp_source_tables` (ERP Source Data) **  
   - Verifies **data integrity and completeness** of ERP records.  
   - Identifies **duplicate transactions, incorrect formats, and inconsistencies**.  

---

##  **Gold Layer Quality Checks**  

 **`gold_layer` (Final Analytical Data) **  
   - **Comprehensive quality checks** for business-ready reports and analytics.  
   - Ensures **star schema integrity**, referential integrity, and **normalized data**.  
   - Detects anomalies in **aggregations, KPIs, and time-series data**.  
   - Validates business rules and ensures **actionable insights** for stakeholders.  

---

**Why Quality Checks Matter?**  
✔️**Prevents data corruption & errors** in analysis.  
✔️ **Enhances data trustworthiness** for decision-making.  
✔️ **Improves reporting accuracy** for stakeholders.  

**"Clean data = Powerful Insights!"** 

** For more details, see the `scripts/` directory in this repository. **

