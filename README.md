# 🌐 AdventureWorks: End-to-End Azure Data Engineering Project

This project demonstrates an enterprise-grade **Data Engineering Pipeline** using Microsoft's Azure ecosystem, built on top of the AdventureWorks dataset. The pipeline covers everything from data ingestion to transformation, warehousing, and final BI reporting.

## 📊 Tools Used

- **Azure Data Factory (ADF)** – Orchestration & automation
- **Azure Data Lake Storage** – Bronze, Silver, and Gold zones for raw to curated data
- **Azure Databricks** – Data transformation using notebooks
- **Azure Synapse Analytics** – Data warehousing using serverless SQL pools
- **Power BI** – Dashboarding and visualization

---

## 🔧 Architecture Overview

![Architecture](images/architecture.png)

---

## ⚙️ Step 1: Azure Resources Provisioning

Provisioned the following cloud resources and configured IAM for secure access:

- Azure Data Factory
- Azure Storage Account with hierarchical namespace (Data Lake)
- Azure Databricks workspace and cluster
- Azure Synapse SQL Serverless
- Power BI Service

![Azure Resources](images/step1-resources.png)

---

## 🚀 Step 2: Data Ingestion via ADF

Using **HTTP connector**, ADF pipelines fetch AdventureWorks data from GitHub and drop into the `bronze` container.

- Dynamic parameters and datasets
- Logging and error handling enabled

![ADF Ingestion](images/step2-adf-pipeline.png)

---

## 🔄 Step 3: Transformation Using Databricks

Azure Databricks processes data from bronze to silver with transformations:

- Cleaned missing values
- Date normalization
- Grouping, joins, and aggregations
- Output saved in **Parquet** format

![Databricks Notebook](images/step3-databricks1.png)
![Databricks Output](images/step3-databricks2.png)

---

## 🧠 Step 4: Data Modeling in Synapse Analytics

- Connected Synapse to **Silver** data
- Created external tables and views
- Designed schema for analytical consumption

![Synapse Tables](images/step4-synapse-tables.png)
![Synapse Queries](images/step4-synapse-query.png)

---

## 📊 Step 5: BI Integration with Power BI

Power BI connected to Synapse SQL and visualized key metrics:

- Sales performance by region & product
- Year-over-year growth
- Category and subcategory analysis

![Power BI Report 1](images/step5-powerbi1.png)
![Power BI Report 2](images/step5-powerbi2.png)
![Power BI Report 3](images/step5-powerbi3.png)

---

## ✅ Outcome & Learnings

| Key Benefit       | Description                                        |
|-------------------|----------------------------------------------------|
| 🚀 Automation     | Full ETL flow without manual steps                 |
| 🧱 Modular Design | Bronze → Silver → Gold architecture                |
| 🔍 BI Ready       | Power BI dashboards refresh automatically          |
| 💡 Scalable       | All services scale on-demand for future growth     |

---

## 📁 Folder Structure

```bash
azure-adventureworks-pipeline/
├── adf/
│   └── pipeline.json
├── databricks/
│   └── notebooks.ipynb
├── synapse/
│   └── external_tables.sql
├── powerbi/
│   └── dashboards.pbix
├── images/
│   └── (11 images referenced above)
└── README.md
```

---

## 🙌 Acknowledgment

This project is inspired by the Azure Data Engineering approach presented by **Sivaprasad V**. 

---

## ✉️ Contact

- 📧 your.email@example.com
- 🔗 [LinkedIn](https://linkedin.com/in/your-profile)
