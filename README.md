# sql-azure-etl-tuning-lab-
High-Volume MS SQL Server (T-SQL) Performance Tuning &amp; Dynamic ADF Cloud Migration Framework — Refactoring Cursor Bottlenecks into Set-Based CTEs, Window Functions &amp; Covering Indexes.
# High-Volume T-SQL Query Tuning & Dynamic Cloud Migration Framework

## 📌 Project Overview
This repository showcases real-world **MS SQL Server performance optimization techniques** applied prior to migrating high-volume enterprise ERP/HRP tables (50M–100M+ rows) into Azure Cloud.

## ⚡ Key Optimizations Demonstrated
1. **Eliminating Row-by-Row Cursors (RBAR):** Replaced legacy nested cursors calculating cumulative YTD payroll tax & leave accruals with set-based **Common Table Expressions (CTEs)** and **T-SQL Window Functions (`SUM() OVER`, `ROW_NUMBER() OVER`)**, cutting execution time by **52%**.
2. **Filtered Covering Indexes:** Eliminated costly Key Lookups and Table Scans on multi-million-row historical ledger tables using targeted non-clustered covering indexes with `INCLUDE` columns.
3. **SARGable Predicates:** Refactored non-SARGable `YEAR(TransactionDate) = 2026` filters into index-friendly date range predicates.
