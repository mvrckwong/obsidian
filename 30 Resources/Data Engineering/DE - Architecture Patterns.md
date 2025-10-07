---
type: resource
source: Industry Knowledge
topic: Data Architecture
date_added: 2025-10-05
tags:
  - data-engineering
  - architecture
  - patterns
  - streaming
  - batch
---

# Data Architecture Patterns

Common architectural patterns for designing scalable, reliable data systems.

## Summary
- Different use cases require different architectural approaches
- Key decision: batch vs. streaming vs. hybrid processing
- Trade-offs between complexity, cost, latency, and reliability

## Key Patterns

### 1. Batch Processing
**What it is:** Process data in large chunks at scheduled intervals (hourly, daily, weekly)

**Best for:**
- Historical analytics and reporting
- Large-volume ETL jobs
- Cost-sensitive workloads
- When real-time isn't required

**Typical Tools:**
- dbt for transformations
- Airflow for orchestration
- Spark for heavy processing
- Cloud warehouses (Snowflake, BigQuery)

**Trade-offs:**
- ✅ Simple, well-understood patterns
- ✅ Cost-effective for large volumes
- ✅ Easy to debug and reprocess
- ❌ Higher latency (hours to days)
- ❌ Not suitable for real-time use cases

---

### 2. Stream Processing
**What it is:** Process data continuously as it arrives, event by event

**Best for:**
- Real-time dashboards and alerts
- Fraud detection
- Personalization engines
- IoT and sensor data
- Operational analytics

**Typical Tools:**
- Kafka or Kinesis for streaming
- Flink, Spark Streaming, or Kafka Streams for processing
- ClickHouse or Druid for real-time analytics

**Trade-offs:**
- ✅ Low latency (seconds to minutes)
- ✅ Enables real-time applications
- ✅ Continuous processing
- ❌ More complex to build and maintain
- ❌ Higher infrastructure costs
- ❌ Harder to debug and reprocess

---

### 3. Lambda Architecture
**What it is:** Hybrid approach with both batch and speed layers, merged at serving layer

**Architecture:**
```
Data Sources → Batch Layer (complete, accurate)
            → Speed Layer (fast, approximate)
            → Serving Layer (merged view)
```

**Best for:**
- When you need both accuracy and low latency
- Transitioning from batch to streaming
- Complex aggregations that are expensive in real-time

**Trade-offs:**
- ✅ Best of both worlds (accuracy + speed)
- ✅ Fault tolerance through batch recomputation
- ❌ Maintain two processing systems
- ❌ Reconciliation complexity
- ❌ Higher operational overhead

---

### 4. Kappa Architecture
**What it is:** Streaming-first architecture, everything is a stream

**Architecture:**
```
Data Sources → Streaming Layer → Serving Layer
                    ↓
              Reprocessing through same stream
```

**Best for:**
- True real-time requirements
- When batch layer adds unnecessary complexity
- Event-driven systems
- Modern cloud-native applications

**Trade-offs:**
- ✅ Single processing paradigm
- ✅ Simpler than Lambda (no batch layer)
- ✅ Reprocessing via stream replay
- ❌ Requires stream-first thinking
- ❌ Can be expensive for large historical data
- ❌ Complex state management

---

### 5. Data Mesh
**What it is:** Decentralized data ownership with domain-oriented data products

**Core Principles:**
1. **Domain Ownership**: Teams own their data products
2. **Data as a Product**: Each dataset treated as a product with SLAs
3. **Self-Service Platform**: Infrastructure abstraction for domains
4. **Federated Governance**: Automated, computational governance

**Best for:**
- Large organizations with multiple domains
- When centralized data teams become bottlenecks
- Mature data organizations (Level 4+)

**Trade-offs:**
- ✅ Scales with organization
- ✅ Domain teams move faster
- ✅ Reduces central team bottleneck
- ❌ Requires organizational maturity
- ❌ Complex governance and standards
- ❌ Potential data duplication

---

### 6. Micro-Batch Processing
**What it is:** Small, frequent batch jobs (every few minutes)

**Best for:**
- "Near real-time" requirements (5-15 minute latency OK)
- Simpler than full streaming
- Cost-conscious teams

**Typical Tools:**
- dbt with frequent schedules
- Airflow with short intervals
- Spark in micro-batch mode

**Trade-offs:**
- ✅ Simpler than streaming
- ✅ Good balance of latency and complexity
- ✅ Leverage batch tooling
- ❌ Still not "real-time"
- ❌ May not scale to high volumes

---

## Decision Framework

**Choose Batch when:**
- Latency requirements > 1 hour
- Data volume is very large
- Team has strong SQL skills
- Cost optimization is critical

**Choose Streaming when:**
- Latency requirements < 5 minutes
- Real-time alerts or dashboards needed
- Event-driven use cases
- You have streaming expertise

**Choose Micro-Batch when:**
- Latency requirements 5-60 minutes
- Want simplicity of batch with better latency
- Transitioning to real-time

**Choose Lambda when:**
- Need both accuracy and speed
- Complex aggregations
- Can afford operational complexity

**Choose Kappa when:**
- Everything must be real-time
- Strong streaming team
- Event sourcing makes sense

**Choose Data Mesh when:**
- Large, multi-domain organization
- Centralized teams are bottlenecks
- High organizational maturity

## How I'll Use This
- Evaluate architecture for new data products
- Make informed trade-offs between patterns
- Communicate options to stakeholders with pros/cons

## Related Projects / Areas
- [[DE - Index]]
- [[Core Data Engineering Stack]]
- [[DE - Maturity Model]]

> PARA Resource: Architectural patterns for designing data systems.
