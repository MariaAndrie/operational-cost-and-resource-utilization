# Operational Cost & Resource Utilization Analysis

## Overview

This project analyzes operational cost, budget variance, resource utilization, overtime, and cost drivers in a synthetic IT Operations environment.

The dashboard focuses on **2025 performance compared with 2024** and shows how cost pressure increased while staffing capacity remained broadly flat.

## Dashboard Preview

![Dashboard Preview](images/operational_cost_resource_dashboard.png)

## Business Questions

- Are operating costs within budget?
- Which cost categories drive the budget overrun?
- Are higher costs connected to resource pressure and overtime?
- Which teams show the clearest utilization pressure?
- Where should management focus cost control and capacity planning?

## Tools

- MySQL
- SQL
- Power BI

## Data Model

Main tables used:

- `fact_costs`
- `fact_cost_details`
- `fact_capacity`
- `fact_tickets`
- `dim_date`
- `dim_team`
- `dim_region`
- `dim_service`

The dataset covers **2024–2025** and represents an IT Operations environment with cost, capacity, and ticket activity data.

## Power BI Dashboard

The Power BI report is a one-page executive dashboard:

**Executive Cost Overview**

Main dashboard sections:

- 2025 KPI cards with comparison vs 2024
- Budget vs actual cost trend
- Budget variance by cost category
- Resource utilization by team and month
- Overtime trend

Dashboard story:

> 2025 cost pressure increased as overtime rose sharply while staffing remained flat.

## Key KPIs

| KPI | 2024 | 2025 |
|---|---:|---:|
| Total Budget | 38.62M | 38.73M |
| Actual Cost | 39.03M | 40.21M |
| Budget Variance | 410.29K | 1.47M |
| Budget Variance % | 1.06% | 3.80% |
| Resource Utilization % | 87.78% | 88.20% |
| Overtime Hours | 1.92K | 8.74K |
| Overtime Rate | 0.24% | 1.10% |

## Key Findings

- Actual cost exceeded budget by **$1.47M** in 2025.
- Budget variance increased from **$410.29K in 2024** to **$1.47M in 2025**.
- Overtime hours increased from **1.92K** to **8.74K**.
- Network Operations showed the clearest resource pressure, especially during May-August.
- Salary was the largest absolute budget variance driver.
- Contractors and software added further cost pressure.

## Recommended Actions

- Review Network Operations capacity during May–August, where utilization exceeded 100% and overtime increased.
- Monitor contractor and software costs as secondary drivers of the 2025 budget overrun.
- Use overtime and utilization trends as early indicators for capacity planning and cost control.


## 2025 Cost Category Variance

| Cost Category | Budget Variance | Variance Rate |
|---|---:|---:|
| Salary | 901.35K | 3.33% |
| Contractors | 287.69K | 4.94% |
| Software | 184.57K | 5.93% |
| Training | 52.73K | 3.41% |
| Travel | 44.73K | 3.84% |

## SQL Work Completed

SQL files:

- `sql/03_data_quality_checks.sql`
- `sql/04_business_logic_validation.sql`
- `sql/05_cost_kpi_analysis.sql`

SQL work includes:

- Data quality checks
- Cost and capacity validation
- Budget vs actual analysis
- Resource utilization checks
- Overtime analysis
- Cost category variance analysis
- 2025 vs 2024 KPI comparison


## Project Structure

```text
operational-cost-resource-utilization-analysis/
│
├── data/
│   ├── dim_date.csv
│   ├── fact_tickets.csv
│   ├── fact_capacity.csv
│   ├── fact_costs.csv
│   └── ...
│
├── sql/
│   ├── 03_data_quality_checks.sql
│   ├── 04_business_logic_validation.sql
│   └── 05_cost_kpi_analysis.sql
│
├── powerbi/
│   └── Operational_Cost_Resource_Utilization.pbix
│
├── images/
│   └── operational_cost_resource_dashboard.png
│
└── README.md
```

## Project Purpose

This project demonstrates practical Operations Analytics skills:

- SQL-based data validation
- Cost control analysis
- Budget variance analysis
- Resource utilization analysis
- Capacity and overtime analysis
- Power BI executive dashboard design
