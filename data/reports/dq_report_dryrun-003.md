# ETL Data Quality & Execution Report — Batch `dryrun-003`

**Status:** `SUCCESS`  
**Mode:** `full` | **Dry Run:** `True`  
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

## 4. Stage Execution Timings

| Stage | Duration (ms) |
| :--- | ---: |
| `extract` | 37.02 |
| `validate` | 678.62 |
| `transform` | 115.77 |
| `total_pipeline` | 832.10 |
