
# Data Quality and Validation Checklist

## Project
Accounting & Financial Reporting — Nusantara Office Supplies

## Reporting Period
1 January 2025 – 31 December 2025

## Validation Objectives

To ensure that all source datasets are complete, consistent, accurate, and suitable for accounting processing.

## 1. Completeness Checks

- [ ] Confirm all expected CSV files are available.
- [ ] Check required columns in each dataset.
- [ ] Identify missing transaction IDs.
- [ ] Review blank values in critical fields.

## 2. Duplicate Checks

- [ ] Check duplicate invoice IDs and line references.
- [ ] Check duplicate purchase IDs.
- [ ] Check duplicate receipt IDs.
- [ ] Check duplicate payment IDs.

## 3. Referential Integrity

- [ ] Match sales invoice IDs with customer receipts.
- [ ] Match purchase IDs with supplier payments.
- [ ] Match expense IDs with operating expense payments.
- [ ] Match product SKUs with the product master.

## 4. Financial Accuracy

- [ ] Recalculate sales amounts.
- [ ] Recalculate purchase amounts.
- [ ] Reconcile customer receipts.
- [ ] Reconcile supplier payments.
- [ ] Verify opening trial balance equality.

## 5. Inventory Validation

- [ ] Verify opening inventory values.
- [ ] Recalculate moving weighted-average costs.
- [ ] Check for negative inventory quantities.
- [ ] Reconcile ending inventory quantities and values.

## 6. Validation Results

Results will be documented after performing the actual checks.

No validation status should be marked as passed without supporting evidence.

**Status:** Pending validation.
