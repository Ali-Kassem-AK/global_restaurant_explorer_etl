# ETL Data Quality & Execution Report — Batch `idempotency-run-002`

**Status:** `SUCCESS`  
**Mode:** `full` | **Dry Run:** `False`  
**Source File:** `zomato_cleaned.csv` (`b7b827b6a61a23b281af014b5622a0f5cc979052b107269fe54e841a233eb27e`)  
**Database Dialect:** `sqlite` | **Storage Backend:** `local`

## 1. Record Processing Summary

| Metric | Count |
| :--- | ---: |
| Extracted Rows | 9,550 |
| Accepted Rows | 9,550 |
| Quarantined (Rejected) Rows | 0 |
| Silver Restaurants Inserted | 0 |
| Silver Restaurants Updated | 0 |
| Silver Restaurants Unchanged | 9,550 |

## 2. Data Quality Findings

| Severity | Count |
| :--- | ---: |
| CRITICAL | 0 |
| ERROR | 0 |
| WARNING | 497 |
| INFO | 14 |

### Issues by Type

| Issue Type | Count |
| :--- | ---: |
| `MISSING_COORDINATES` | 497 |
| `MISSING_CUISINES` | 9 |
| `DUPLICATE_CUISINE_IN_ROW` | 5 |

## 3. Gold Layer Verification

| View Name | Row Count | Query Latency (ms) |
| :--- | ---: | ---: |
| `v_restaurant_explorer` | 9,550 | 6.30 |
| `gold_restaurant_search` | 9,550 | 30.13 |
| `gold_city_restaurant_stats` | 141 | 14.82 |
| `gold_country_restaurant_stats` | 15 | 9.78 |
| `gold_cuisine_stats` | 145 | 24.91 |
| `gold_price_range_stats` | 4 | 4.83 |
| `gold_rating_distribution` | 33 | 7.60 |
| `gold_geographic_coverage` | 141 | 10.72 |

## 4. Stage Execution Timings

| Stage | Duration (ms) |
| :--- | ---: |
| `extract` | 65.53 |
| `validate` | 676.26 |
| `transform` | 142.22 |
| `silver_load` | 242.30 |
| `gold_refresh` | 159.41 |
| `total_pipeline` | 1337.02 |
