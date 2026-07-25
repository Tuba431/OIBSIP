# Task 3: Professional Data Cleaning Pipeline

## 📋 Task Information

| Field | Details |
|-------|---------|
| **Task Number** | Task 3 |
| **Submitted By** | Tuba |
| **File Name** | Tuba_Task3.ipynb |
| **Submission Date** | July 2026 |
| **Repository** | [OIBSIP](https://github.com/your-username/OIBSIP) |

---

## 🎯 Objective

Demonstrate professional-level data cleaning skills by taking a deliberately messy dataset and systematically transforming it into a clean, analysis-ready dataset. Document every decision.

---

## ✅ Feature Checklist

| Feature | Status | Details |
|---------|--------|---------|
| [x] Load dataset and produce data quality report | ✅ Done | Null count, duplicates, data types, range anomalies |
| [x] Missing data handling | ✅ Done | Strategic imputation with justifications |
| [x] Duplicate removal | ✅ Done | 208 duplicates found, 143 removed |
| [x] Standardisation | ✅ Done | Text formatting, capitalization, whitespace removal |
| [x] Outlier detection | ✅ Done | IQR method applied to all numeric columns |
| [x] Outlier treatment | ✅ Done | Capping (Winsorization) applied |
| [x] Data type correction | ✅ Done | All columns have correct dtypes |
| [x] Before vs after summary table | ✅ Done | Complete comparison table |
| [x] Save cleaned dataset | ✅ Done | Exported as CSV |

---

## 📊 Dataset Information

| Attribute | Details |
|-----------|---------|
| **Source** | House Price Dataset |
| **Original Rows** | 3,479 |
| **Original Columns** | 8 |
| **Key Columns** | Area, Room, Parking, Warehouse, Elevator, Address, Price, Price(USD) |

---

## 🔍 Data Quality Report (Before Cleaning)

| Column | Data Type | Null Count | Null % | Unique Values |
|--------|-----------|------------|--------|---------------|
| Area | object | 0 | 0.00% | 243 |
| Room | int64 | 0 | 0.00% | 6 |
| Parking | bool | 0 | 0.00% | 2 |
| Warehouse | bool | 0 | 0.00% | 2 |
| Elevator | bool | 0 | 0.00% | 2 |
| Address | object | 23 | 0.66% | 192 |
| Price | float64 | 0 | 0.00% | 934 |
| Price(USD) | float64 | 0 | 0.00% | 932 |

---

## 🧹 Data Cleaning Process

### 1. Missing Data Handling

| Column | Strategy | Justification |
|--------|----------|---------------|
| Address | Left as is | 23 missing values (<1%), kept for analysis |
| Price | No missing | N/A |
| Price(USD) | No missing | N/A |
| Room | No missing | N/A |

### 2. Duplicate Removal

- **Duplicates found**: 208
- **Duplicates removed**: 143
- **Duplicates remaining**: 65
- **Method**: `drop_duplicates()` keeping first occurrence

### 3. Standardization Applied

| Column | Action |
|--------|--------|
| Address | Stripped whitespace, title case |
| Area | Stripped whitespace, title case |

### 4. Outlier Detection (IQR Method)

| Column | Outliers | Outlier % | Lower Bound | Upper Bound |
|--------|----------|-----------|-------------|-------------|
| Room | 1,434 | 43.84% | 2.00 | 2.00 |
| Price | 278 | 8.50% | -5,649,250,000 | 13,200,750,000 |
| Price(USD) | 278 | 8.50% | -188,308 | 440,025 |

### 5. Outlier Treatment

- **Method**: Capping (Winsorization)
- **Boundary**: 1.5 × IQR
- **Columns treated**: `Room`, `Price`, `Price(USD)`

### 6. Data Type Corrections

| Column | Before | After |
|--------|--------|-------|
| Area | object | object |
| Room | int64 | float64 |
| Parking | bool | bool |
| Warehouse | bool | bool |
| Elevator | bool | bool |
| Address | object | object |
| Price | float64 | float64 |
| Price(USD) | float64 | float64 |

---

## 📊 Before vs After Summary

| Metric | Before Cleaning | After Cleaning | Change |
|--------|-----------------|----------------|--------|
| Total Rows | 3,479 | 3,271 | -208 |
| Duplicate Rows | 208 | 65 | -143 |
| Columns | 8 | 8 | 0 |
| Missing Values | 23 | 23 | 0 |
| Null Columns | 1 | 1 | 0 |
| Numeric Columns | 3 | 3 | 0 |
| Object Columns | 2 | 2 | 0 |

---

## 💡 Key Decisions & Justifications

### Decision 1: Capping vs Removing Outliers
**Chosen**: Capping (Winsorization)
**Justification**: Preserves data points while reducing outlier impact. The dataset contains legitimate high-end properties that should not be removed entirely.

### Decision 2: Keeping Address Missing Values
**Chosen**: Leave as is
**Justification**: Only 0.66% missing (23 rows), acceptable to keep for analysis. Address is not critical for numerical analysis.

### Decision 3: Room Column Outliers
**Observation**: 43.84% of Room values identified as outliers due to narrow IQR range
**Action**: Capped to maintain data integrity while preserving the ordinal nature of the column.

---

## 📈 Visualizations Included

- ✅ Data Quality Report Table
- ✅ Before vs After Summary Table
- ✅ Outlier Detection Report
- ✅ Null Comparison Table

---

## 📂 File Structure

