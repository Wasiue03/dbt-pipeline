# dbt + Airflow (Astronomer) + Snowflake Pipeline 🚀

This repository contains an end-to-end **data transformation pipeline** built using:

- **dbt** for transformations
- **Apache Airflow** (via Astronomer)
- **Cosmos** for dbt–Airflow integration
- **Snowflake** as the data warehouse

The project demonstrates how to orchestrate dbt models in Airflow **without manually writing dbt BashOperators**, using Cosmos’ `DbtDag`.

---

## 🏗️ Architecture Overview

```text
Snowflake (Source Tables)
        ↓
     dbt models
        ↓
Cosmos DbtDag
        ↓
   Airflow DAG
