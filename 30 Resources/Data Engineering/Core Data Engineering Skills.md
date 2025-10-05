---
type: resource
source: Industry Standards
topic: Technical Skills
date_added: 2025-10-05
tags:
  - data-engineering
  - skills
  - learning
  - technical
  - career
---

# Core Data Engineering Skills

Essential technical skills for modern data engineers.

## Summary
- Data engineering requires a blend of programming, data modeling, distributed systems, and cloud knowledge
- SQL and Python are foundational
- Depth in a few areas beats shallow knowledge across many tools

## Technical Skills

### 1. SQL (Essential)
**Why it matters:** The universal language of data

**What to learn:**
- Complex joins and subqueries
- Window functions (ROW_NUMBER, LAG, LEAD)
- CTEs (Common Table Expressions)
- Query optimization and execution plans
- Indexing strategies
- Different SQL dialects (PostgreSQL, T-SQL, etc.)

**Proficiency levels:**
- Junior: Basic SELECT, JOIN, WHERE, GROUP BY
- Mid: Window functions, CTEs, query optimization
- Senior: Explain plans, index design, performance tuning at scale

---

### 2. Python (Essential)
**Why it matters:** Most versatile language for data engineering

**What to learn:**
- Data manipulation: Pandas, Polars
- APIs and web scraping: Requests, BeautifulSoup
- Database connectors: SQLAlchemy, psycopg2
- Workflow tools: Airflow, Prefect
- Testing: pytest, unittest
- Package management: pip, poetry, conda

**Common use cases:**
- Building custom data pipelines
- API integrations
- Data validation and quality checks
- Orchestration (Airflow DAGs)
- Infrastructure as code (Terraform Python SDK)

---

### 3. Apache Spark / PySpark (Important for scale)
**Why it matters:** Industry standard for big data processing

**What to learn:**
- DataFrame API
- Spark SQL
- RDDs (less common now, but good to understand)
- Partitioning and optimization
- Cluster computing concepts
- Memory management and caching

**When you need it:**
- Data > 100GB+
- Complex transformations at scale
- ML feature engineering
- Real-time stream processing (Structured Streaming)

---

### 4. Git & GitHub (Essential)
**Why it matters:** Version control is non-negotiable for modern data engineering

**What to learn:**
- Basic commands: clone, pull, push, commit
- Branching strategies (Git Flow, trunk-based)
- Pull requests and code reviews
- Merge conflict resolution
- Git hooks for automation
- .gitignore for sensitive data

**Best practices:**
- Never commit credentials
- Use feature branches
- Write descriptive commit messages
- Keep PRs small and focused

---

### 5. Data Pipelines & ETL/ELT (Essential)
**Why it matters:** Core responsibility of data engineers

**Concepts to understand:**
- ETL vs. ELT patterns
- Incremental vs. full refresh
- Idempotency and exactly-once processing
- Backfilling strategies
- Data validation and testing
- Error handling and retries
- Pipeline orchestration

**Tools:**
- dbt (SQL-based transformations)
- Airflow, Prefect (orchestration)
- Airbyte, Fivetran (ingestion)
- Custom Python scripts

---

### 6. Cloud Platforms (Choose one, learn deeply)
**Why it matters:** Most modern data infrastructure is cloud-native

**AWS:**
- S3 (storage)
- Redshift (data warehouse)
- Glue (ETL)
- Lambda (serverless compute)
- IAM (permissions)

**GCP:**
- BigQuery (data warehouse)
- Cloud Storage
- Dataflow (ETL)
- Cloud Functions
- Cloud Composer (managed Airflow)

**Azure:**
- Azure Data Lake
- Synapse Analytics
- Data Factory
- Azure Functions

**Core concepts across clouds:**
- Object storage
- Data warehouses
- IAM and security
- Networking basics
- Cost management

---

### 7. Data Modeling (Important)
**Why it matters:** Structure drives usability and performance

**What to learn:**
- Dimensional modeling (Kimball): star schema, snowflake schema
- Slowly Changing Dimensions (SCD Types 1, 2, 3)
- Data normalization (1NF, 2NF, 3NF)
- Data Vault 2.0
- Wide tables vs. normalized tables
- ER diagrams

**When to use what:**
- Star schema: Analytics and BI
- Normalized: Transactional systems (OLTP)
- Data Vault: Enterprise data warehouses
- Wide tables: Modern cloud warehouses (Snowflake, BigQuery)

---

### 8. Linux/Unix & Command Line (Helpful)
**Why it matters:** Servers run on Linux; CLI is faster than GUI

**What to learn:**
- Basic commands: ls, cd, grep, find, cat, less
- File permissions and ownership
- Environment variables
- Shell scripting (Bash)
- SSH and remote access
- Package managers (apt, yum)
- Process management (ps, top, kill)

---

### 9. Docker & Containerization (Increasingly important)
**Why it matters:** Standardizes environments, enables reproducibility

**What to learn:**
- Docker basics: images, containers, Dockerfile
- Docker Compose for multi-container apps
- Container orchestration concepts (Kubernetes basics)
- Use cases: local development, CI/CD, production deployment

---

### 10. Data Engineering Project Experience (Essential)
**Why it matters:** Hands-on building is how you truly learn

**Project ideas:**
- End-to-end pipeline: source → warehouse → dashboard
- Build a personal data platform (collect, transform, analyze your own data)
- Real-time streaming pipeline (Kafka → processing → storage)
- dbt project with testing and documentation
- Airflow DAGs for complex workflows

**Portfolio components:**
- GitHub repo with clean code
- README explaining architecture
- Documentation and tests
- Deployed and running (bonus)

---

## Skill Development Path

### Junior Data Engineer (0-2 years)
- Strong SQL
- Python basics
- Git fundamentals
- Understanding of ETL concepts
- Exposure to one data warehouse
- Basic data modeling

### Mid-Level Data Engineer (2-5 years)
- Advanced SQL optimization
- Python for complex pipelines
- Spark for big data
- Cloud platform proficiency
- Pipeline orchestration (Airflow)
- Data modeling expertise
- Performance tuning

### Senior Data Engineer (5+ years)
All of the above, plus:
- Architecture design
- Cross-team collaboration
- Mentoring junior engineers
- Strategic technology decisions
- Cost optimization at scale
- Incident response leadership

---

## How to Learn

### Structured Learning
- Online courses: DataCamp, Udemy, Coursera
- Books: "Designing Data-Intensive Applications", "Fundamentals of Data Engineering"
- Certifications: AWS, GCP, Databricks, dbt

### Hands-On Practice
- Build projects (most important!)
- Contribute to open source
- Kaggle datasets for practice
- Set up your own data infrastructure

### Community
- Join data engineering communities (Slack, Discord, Reddit)
- Attend meetups and conferences
- Follow industry leaders on Twitter/LinkedIn
- Read data engineering blogs

## How I'll Use This
- Self-assessment to identify skill gaps
- Create learning roadmap
- Prioritize depth over breadth
- Build portfolio projects

## Related Projects / Areas
- [[Data Engineering Index]]
- [[Core Data Engineering Stack]]
- [[Data Engineering Soft Skills]]

> PARA Resource: Technical skills roadmap for data engineers.
