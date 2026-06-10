# d8a.academy course datasets

Free, ready-to-use datasets for the [d8a.academy](https://d8a.academy) projects. They
are **synthetic** (generated, no real personal data) and model two fictional companies:

- **Lumen**, a streaming service (used across the Data Science path)
- a small **e-commerce shop** (used across the Data Analyst path)

You don't need to clone this repo. Each lesson links the file it needs. To grab one
yourself, download it from the `main` branch.

## Data Science (Lumen)

| File | Used in | Rows |
| --- | --- | --- |
| `lumen_users.csv` | Descriptive statistics | ~50k |
| `lumen_ab_test.csv` | Hypothesis testing | ~20k |
| `lumen_subscriptions.csv` | Churn classification | ~30k |
| `lumen_watch_target.csv` | Regression | ~30k |
| `lumen_payments.csv` | Fraud detection / feature engineering | ~80k |
| `lumen_streaming_daily.csv` | Time-series forecasting (4 regions) | ~6k |
| `lumen_reviews.csv` | NLP / sentiment (6 languages) | ~30k |

```python
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/d8a-academy/datasets/main/lumen_users.csv")
```

Or download to a file:

```bash
curl -LO https://raw.githubusercontent.com/d8a-academy/datasets/main/lumen_users.csv
```

## Data Analyst (e-commerce)

Files live under [`da/`](da):

| File | Used in |
| --- | --- |
| `da/customers.csv`, `da/orders.csv`, `da/products.csv` | Python, DuckDB & Polars analysis |
| `da/daily_revenue.parquet` | AI-augmented anomaly detection |
| `da/events/events_*.parquet` | DuckDB Parquet queries |

```bash
mkdir -p data
curl -L -o data/orders.csv    https://raw.githubusercontent.com/d8a-academy/datasets/main/da/orders.csv
curl -L -o data/customers.csv https://raw.githubusercontent.com/d8a-academy/datasets/main/da/customers.csv
curl -L -o data/products.csv  https://raw.githubusercontent.com/d8a-academy/datasets/main/da/products.csv
```

> Heads up: `da/orders.csv` intentionally contains some missing values, duplicates and
> inconsistent formatting. That's on purpose, the data-cleaning lesson asks you to fix it.

## A note on the data

Everything here is generated synthetic data for learning. Any names, companies, and
values are fictional and carry no real personal information.
