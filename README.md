# Modern Data Engineering Pipeline

![Python](https://img.shields.io/badge/Python-3.10-blue) ![Airflow](https://img.shields.io/badge/Orchestration-Apache%20Airflow-orange) ![dbt](https://img.shields.io/badge/Transformation-dbt%20Core-FF694B) ![Snowflake](https://img.shields.io/badge/Warehouse-Snowflake-29B5E8)

## 1. Introduction
This project demonstrates an end-to-end data engineering pipeline designed to handle modern data needs. It automates the extraction, loading, and transformation (ELT) of raw data into analytics-ready models.

Built with **Python**, **Apache Airflow**, **Snowflake**, and **dbt**, this repository serves as a comprehensive example of the skills required for Data Engineering and Analytics Engineering roles, focusing on modularity, data quality, and automation.

---

## 2. Architecture
The pipeline follows a standard ELT architecture.


*(Note: Replace the image tag above with the actual path to your architecture diagram PNG file)*

---

## 3. Tech Stack

| Category | Technology | Description |
| :--- | :--- | :--- |
| **Language** | ![Python](https://img.shields.io/badge/-Python_3.10-blue) | Core logic and custom operators |
| **Orchestration** | ![Airflow](https://img.shields.io/badge/-Apache_Airflow-orange) | Scheduling and monitoring workflows |
| **Data Warehouse** | ![Snowflake](https://img.shields.io/badge/-Snowflake-29B5E8) | Storage and compute engine |
| **Transformation** | ![dbt](https://img.shields.io/badge/-dbt_Core-FF694B) | SQL-based transformations and testing |
| **CI/CD** | ![GitHub Actions](https://img.shields.io/badge/-GitHub_Actions-black) | Automated testing and deployment |

---

## 4. Key Features
* **Automated Ingestion:** Custom Python scripts to extract data from APIs/Source systems.
* **Data Quality Checks:** Integrated testing using dbt (schema tests, referential integrity).
* **Modular Transformations:** Layered modeling approach (Staging → Intermediate → Marts).
* **Infrastructure as Code:** Airflow DAGs and dbt models are version controlled.
* **CI/CD Integration:** Automated linting and testing via GitHub Actions on pull requests.

---

## 5. Pipeline Steps
The data flows through the following stages:

1.  **Extract:** Python scripts load raw data from the source.
2.  **Load:** Data is staged in the **Snowflake** (or DuckDB) raw layer.
3.  **Transform:** **dbt** performs data cleaning, casting, and business logic application.
4.  **Orchestrate:** **Airflow** triggers the tasks in the correct dependency order.
5.  **Serve:** Final `fact` and `dimension` tables are generated for reporting.

---

## 6. How to Run Locally

### Prerequisites
* Docker & Docker Compose
* Python 3.10+
* Git

### Steps

**1. Clone the repository**
```bash
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name
