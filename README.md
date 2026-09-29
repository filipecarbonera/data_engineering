# data_engineering

End-to-end data engineering portfolio project on Google Cloud Platform: extraction from multiple sources, a raw data lake, a BigQuery warehouse modeled with dbt, orchestration with Airflow, infrastructure as code with Terraform, and cost monitoring built in.

> 🚧 Work in progress.

## Architecture

_Diagram coming soon._

```
Sources (Postgres, Firestore, public API)
   → Extraction (Python / Cloud Functions)
   → Cloud Storage (Parquet, raw layer)
   → BigQuery
   → dbt (staging → intermediate → marts) + data quality tests
   → Looker Studio
```

Airflow orchestrates every step, with scheduling and retries.

## Tech stack

| Area | Tools |
|---|---|
| Sources | Postgres, Firestore, public API |
| Extraction | Python, Cloud Functions |
| Storage | Cloud Storage (Parquet) |
| Warehouse | BigQuery |
| Transformation | dbt |
| Orchestration | Airflow |
| Infrastructure | Terraform, Docker |
| CI/CD | GitHub Actions |
| Visualization | Looker Studio |

## Repository structure

```
extraction/         Data generators and extraction scripts
functions/          Cloud Functions
dbt/                dbt project
airflow/dags/       Airflow DAGs
terraform/          GCP infrastructure
docker/             Dockerfiles
.github/workflows/  CI/CD pipelines
```

## Design decisions and trade-offs

_Coming soon._

## Cost monitoring

_Coming soon._

## How to reproduce

_Coming soon. Outline:_

1. Create a GCP project and enable billing export to BigQuery.
2. Copy `.env.example` to `.env` and fill in your values.
3. Run `terraform apply`.
4. Run `docker compose up`.

## Cost optimization results

_Coming soon._
