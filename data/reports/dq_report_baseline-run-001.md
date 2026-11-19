# ETL Data Quality & Execution Report — Batch `baseline-run-001`

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
| Silver Restaurants Inserted | 9,550 |
| Silver Restaurants Updated | 0 |
| Silver Restaurants Unchanged | 0 |

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
| `v_restaurant_explorer` | 9,550 | 5.42 |
| `gold_restaurant_search` | 9,550 | 30.05 |
| `gold_city_restaurant_stats` | 141 | 13.88 |
| `gold_country_restaurant_stats` | 15 | 9.78 |
| `gold_cuisine_stats` | 145 | 27.23 |
| `gold_price_range_stats` | 4 | 4.88 |
| `gold_rating_distribution` | 33 | 7.77 |
| `gold_geographic_coverage` | 141 | 10.96 |

## 4. Stage Execution Timings

| Stage | Duration (ms) |
| :--- | ---: |
| `extract` | 39.94 |
| `bronze` | 1.61 |
| `validate` | 679.26 |
| `transform` | 120.57 |
| `silver_load` | 313.82 |
| `gold_refresh` | 141.70 |
| `total_pipeline` | 1374.40 |
