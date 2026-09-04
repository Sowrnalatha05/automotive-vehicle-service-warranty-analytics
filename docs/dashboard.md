# Automotive Vehicle Service & Warranty Analytics Dashboard

## Dashboard Overview

The Automotive Vehicle Service & Warranty Analytics dashboard provides an interactive view of vehicle servicing, warranty claims, service costs, dealer performance, technician performance, and service-center activity.

The dashboard is built using **Databricks AI/BI Dashboards** and uses business-ready datasets from the **Gold Layer** of the Medallion Architecture.

## Key Performance Indicators

The dashboard contains the following KPI cards:

- **Total Vehicles Serviced** – Total number of vehicles handled through the service process.
- **Total Service Orders** – Total number of service orders processed.
- **Warranty Claims** – Total number of warranty claims submitted.
- **Total Service Cost** – Total labor and parts-related service cost.

## Dashboard Visualizations

### 1. Service Orders by Vehicle Make
Shows the number of service orders associated with each vehicle manufacturer.

**Purpose:** Identify vehicle makes with higher service activity.

### 2. Warranty Claims by Status
Displays warranty claims grouped by their current status.

**Purpose:** Understand approved, rejected, and pending warranty claims.

### 3. Dealer Performance by Service Orders
Shows service-order volume across different dealers.

**Purpose:** Compare dealer activity and identify high-performing service locations.

### 4. Technician Performance by Service Orders
Displays service-order workload handled by technicians.

**Purpose:** Compare technician workloads and identify variations in service activity.

### 5. Service Center by Vehicle Make
Shows service activity by vehicle manufacturer across service centers.

**Purpose:** Understand the distribution of vehicle servicing across service locations.

### 6. Top 10 Service Centers by Service Orders
Displays the service centers with the highest number of service orders.

**Purpose:** Identify the busiest service centers and support operational planning.

## Data Architecture

The dashboard follows the Medallion Architecture:

```text
15 CSV Source Files
        ↓
Bronze Layer
15 Delta Tables
        ↓
Silver Layer
15 Cleaned & Transformed Delta Tables
        ↓
Gold Layer
6 Business-Ready Analytics Tables
        ↓
Databricks AI/BI Dashboard
