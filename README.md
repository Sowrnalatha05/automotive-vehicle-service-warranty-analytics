# Automotive Vehicle Service & Warranty Analytics

## 📌 Project Overview

This project implements an end-to-end **Automotive Vehicle Service and Warranty Analytics** solution using **Databricks, Delta Lake, PySpark, SQL, and Databricks AI/BI Dashboards**.

The solution processes automotive service, vehicle, customer, dealer, technician, parts, and warranty data through a **Medallion Architecture (Bronze → Silver → Gold)** and provides business-ready analytics through an interactive dashboard.

---

## 🎯 Objectives

- Analyze vehicle service activity and service orders
- Monitor warranty claims and claim status
- Analyze service costs and parts/labor expenses
- Evaluate dealer performance
- Evaluate technician performance
- Analyze service center performance
- Provide business insights through an interactive dashboard

---

## 🏗️ Architecture

```text
                 SOURCE DATA
              15 CSV Files
                    │
                    ▼
        ┌──────────────────────┐
        │    BRONZE LAYER      │
        │   15 Delta Tables    │
        │  Raw Data Ingestion  │
        └──────────┬───────────┘
                   │
                   ▼
        ┌──────────────────────┐
        │    SILVER LAYER      │
        │   15 Delta Tables    │
        │ Cleaning &           │
        │ Transformation       │
        └──────────┬───────────┘
                   │
                   ▼
        ┌──────────────────────┐
        │     GOLD LAYER       │
        │   6 Analytics Tables │
        │ Business-Ready Data  │
        └──────────┬───────────┘
                   │
                   ▼
        ┌──────────────────────┐
        │   DATABRICKS AI/BI   │
        │      DASHBOARD       │
        └──────────────────────┘
