# ETL Data Quality & Execution Report — Batch `dcff5e51-76dc-4d89-9e68-bf76c76b460e`

**Status:** `SUCCESS`  
**Mode:** `full` | **Dry Run:** `False`  
**Source File:** `zomato_cleaned.csv` (`b7b827b6a61a23b281af014b5622a0f5cc979052b107269fe54e841a233eb27e`)  
**Database Dialect:** `mysql` | **Storage Backend:** `local`

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
| `v_restaurant_explorer` | 9,550 | 56.56 |
| `gold_restaurant_search` | 9,550 | 448.73 |
| `gold_city_restaurant_stats` | 141 | 142.72 |
| `gold_country_restaurant_stats` | 15 | 104.30 |
| `gold_cuisine_stats` | 145 | 200.46 |
| `gold_price_range_stats` | 4 | 33.60 |
| `gold_rating_distribution` | 33 | 49.40 |
| `gold_geographic_coverage` | 141 | 104.98 |

## 4. Stage Execution Timings

| Stage | Duration (ms) |
| :--- | ---: |
| `extract` | 67.67 |
| `bronze` | 9.54 |
| `validate` | 1634.39 |
| `transform` | 237.20 |
| `silver_load` | 1395.87 |
| `gold_refresh` | 1175.72 |
| `total_pipeline` | 5533.59 |
