# Day 0 – Setup & Data Loading

Day 0 focused on setting up Databricks and loading a real-world dataset.

Unlike ideal tutorials, I faced and resolved several real Databricks-specific issues.
This document captures **what actually happened**, not just the final result.

---

## ✅ What I Did

- Created Databricks Community Edition account
- Set up Kaggle API authentication
- Created Schema and Volume using Unity Catalog
- Downloaded and extracted large CSV datasets (~13M rows)
- Loaded data using Spark

---

## ⚠️ Issues Faced & Fixes

### 1. Kaggle API mismatch
- Tutorial expected `kaggle.json`
- Kaggle provided a single API token instead

**Fix:** Used `KAGGLE_API_TOKEN` environment variable.

---

### 2. Files not visible after download
- Kaggle downloaded files to hidden driver storage
- Could not browse system paths

**Fix:** Downloaded dataset directly into a Databricks Volume.

---

### 3. CSV schema issues
- Spark treated headers as data
- All columns were read as STRING

**Fix:** Enabled `header=True` and `inferSchema=True`.

---

## 📌 Key Learning
- Workspace is for notebooks, not data
- Volumes are the correct place for datasets
- Spark is lazy and schema must be explicit

---

✅ Day 0 complete and ready for real analysis.
