# Databricks AI/BI Dashboard

## Dashboard Overview

The Automotive Vehicle Service & Warranty Analytics dashboard provides an interactive view of vehicle service operations, warranty claims, service costs, dealer performance, technician performance, and service center performance.

The dashboard is built using Databricks AI/BI Dashboards and uses business-ready Gold layer tables created through the Medallion Architecture.

## Key Performance Indicators

- Total Vehicles Serviced: 10K
- Total Service Orders: 10K
- Warranty Claims: 3.5K
- Total Service Cost: 2.48B

## Dashboard Visualizations

The dashboard contains visualizations for:

- Service Orders by Vehicle Make
- Warranty Claims by Status
- Dealer Performance by Service Orders
- Technician Performance
- Service Center Performance
- Service Cost Analysis
- Vehicle Service Analysis

## Data Source

The dashboard uses the following Gold layer tables:

1. `automotive_project.gold.vehicle_service_analysis`
2. `automotive_project.gold.warranty_analysis`
3. `automotive_project.gold.dealer_performance`
4. `automotive_project.gold.service_cost_analysis`
5. `automotive_project.gold.technician_performance`
6. `automotive_project.gold.service_center_performance`

## Architecture

```text
15 CSV Source Files
        |
        v
Bronze Layer
15 Delta Tables
        |
        v
Silver Layer
15 Cleaned & Transformed Delta Tables
        |
        v
Gold Layer
6 Business-Ready Analytics Tables
        |
        v
Databricks AI/BI Dashboard
