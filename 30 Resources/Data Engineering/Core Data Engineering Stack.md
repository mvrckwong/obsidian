---
type: resource
source: Industry Best Practices
topic: Data Engineering Tools
date_added: 2025-10-05
tags:
  - data-engineering
  - tools
  - architecture
  - stack
---

# Core Data Engineering Stack

Essential components and popular tools for building modern data platforms.

## Summary
- Modern data engineering requires five core components: ingestion, orchestration, transformation, storage, and reporting
- Tool selection should balance cost, complexity, team skills, and business requirements
- The "modern data stack" emphasizes SQL-based transformations and cloud-native solutions

## Core Components

### 1. Data Ingestion
**Purpose:** Extract and load data from various sources into your data platform

**Popular Tools:**
- **Airbyte**: Open-source, 300+ connectors, self-hosted or cloud
- **Fivetran**: Managed service, reliable, expensive but low maintenance
- **Stitch**: Simpler managed option from Talend
- **Custom Scripts**: Python/API integrations for unique sources
- **Change Data Capture (CDC)**: Debezium, AWS DMS for real-time replication

**When to use what:**
- Airbyte: Budget-conscious, need custom connectors
- Fivetran: Enterprise, want reliability with minimal maintenance
- Custom: Unique APIs, complex business logic during ingestion

---

### 2. Orchestration
**Purpose:** Schedule, monitor, and manage data pipeline workflows

**Popular Tools:**
- **Apache Airflow**: Industry standard, Python-based DAGs, huge ecosystem
- **Prefect**: Modern alternative, better UI, easier local development
- **Dagster**: Asset-oriented, strong data quality focus
- **Mage.ai**: Notebook-style interface, good for ML workflows
- **Temporal**: For complex, long-running workflows

**When to use what:**
- Airflow: You need battle-tested, have Python engineers
- Prefect: Want modern UX, easier debugging
- Dagster: Data quality is critical, asset-centric thinking

---

### 3. Data Transformation
**Purpose:** Clean, model, and transform raw data into analytics-ready datasets

**Popular Tools:**
- **dbt (data build tool)**: SQL-based, version control, testing, documentation
- **Apache Spark/PySpark**: Large-scale distributed processing
- **Pandas/Polars**: In-memory processing for smaller datasets
- **SQL Views**: Simple transformations directly in warehouse

**When to use what:**
- dbt: Analytical transformations, teams that know SQL
- Spark: Big data (100GB+), complex aggregations, ML feature engineering
- Pandas/Polars: Data science workflows, one-off analyses

---

### 4. Data Storage
**Purpose:** Store processed data for analytics and reporting

**Popular Solutions:**
- **Snowflake**: Excellent performance, easy scaling, can be expensive
- **BigQuery**: Google Cloud, serverless, pay-per-query model
- **Redshift**: AWS native, good for existing AWS shops
- **Databricks**: Spark-based, great for ML and streaming
- **PostgreSQL**: Open-source, good for smaller workloads

**When to use what:**
- Snowflake: Multi-cloud, need separation of compute/storage
- BigQuery: Already on GCP, want serverless simplicity
- Redshift: Heavily invested in AWS ecosystem
- PostgreSQL: Small to medium data, want open-source

---

### 5. Reporting & BI
**Purpose:** Visualize data and deliver insights to stakeholders

**Popular Tools:**
- **Power BI**: Microsoft ecosystem, enterprise features
- **Tableau**: Best-in-class visualizations, more expensive
- **Metabase**: Open-source, simple, good for internal tools
- **Looker**: Code-based (LookML), strong governance
- **Superset**: Open-source alternative to Tableau
- **Streamlit/Dash**: For custom Python dashboards

**When to use what:**
- Power BI: Microsoft shop, need Excel integration
- Metabase: Startups, simple internal dashboards
- Looker: Need version control for metrics, centralized governance
- Streamlit: Custom interactive apps, ML demos

---

## Key Selection Criteria

### Cost Considerations
- Open-source vs. managed services
- Compute costs (per-query vs. always-on)
- Team time (build vs. buy)

### Technical Fit
- Data volume and velocity
- Latency requirements (batch vs. real-time)
- Existing cloud provider
- Team expertise

### Organizational Factors
- Team size and skills
- Support requirements
- Compliance and security needs
- Vendor lock-in tolerance

## Modern Data Stack Philosophy
The "modern data stack" emphasizes:
- Cloud-native and managed services
- SQL as the primary transformation language
- Version control and testing for data code
- Separation of compute and storage
- Modular, best-of-breed tools over monolithic platforms

## How I'll Use This
- Reference when evaluating new tools
- Share with stakeholders to explain architecture
- Update as tools evolve and new solutions emerge

## Related Projects / Areas
- [[Data Engineering Index]]
- [[Data Architecture Patterns]]
- [[Core Data Engineering Skills]]

> PARA Resource: Guide to essential data engineering tools and components.
