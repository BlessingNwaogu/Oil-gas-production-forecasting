## Oil & Gas Production Forecasting with Microsoft Fabric & Power BI

An end-to-end oil & gas production forecasting and scenario-analysis solution built using Microsoft Fabric, Python, ARPS decline-curve modelling, DAX and Power BI.

The project transforms historical well-production data into well-level decline forecasts, portfolio-level production insights and interactive What-If scenarios for operational decision-making.

---

## Business Problem

Oil and gas production naturally declines over time, while operational downtime and well interventions can significantly affect performance.

The goal of this project was to build a solution that could:

- Monitor current production performance
- Forecast future oil production
- Compare actual production against business plans
- Identify wells with high decline rates
- Test operational scenarios such as downtime recovery and workovers
- Make forecast quality transparent to business and engineering users

---

## Solution Architecture

```text
Source Production Data
        ↓
Microsoft Fabric Lakehouse
        ↓
Python / ARPS Forecasting Pipeline
        ↓
Curated Gold Tables
        ↓
Fabric SQL Analytics Endpoint
        ↓
Power BI + DAX
        ↓
Interactive Forecasting & What-If Report

```

---

## Power BI Report

### 1. Portfolio Overview

Provides a high-level view of production performance and outlook, including:

- Current production
- 12-month production forecast
- Month-on-month production movement
- Portfolio natural decline rate
- Recoverable upside scenario
- Production contribution by field
- Wells ranked by decline rate
- Actual vs Business Plan vs ARPS forecast

![Portfolio Overview](Portfolio%20Overview.PNG)

---

### 2. Forecast & What-If

Allows users to dynamically test production scenarios using:

- Decline-rate adjustment
- Downtime reduction
- Workover uplift
- Workover timing

The scenario forecast recalculates dynamically and is compared with the base ARPS forecast.

![Forecast and What-If](Forecast%20%26%20What-If.PNG)

---

### 3. Model Transparency & Diagnostics

Makes the forecasting model inspectable rather than treating it as a black box.

Users can inspect:

- Well-level ARPS parameters
- Initial production rate (`qi`)
- Decline rate (`di`)
- Decline shape (`b`)
- Baseline uptime
- R² model-fit quality
- Actual production
- 7-day production trend
- ARPS fitted decline curve

![Model Transparency](Model%20Transparency.PNG)

---

## Technology Stack

- Microsoft Fabric
- Fabric Lakehouse
- SQL Analytics Endpoint
- Python
- PySpark
- Pandas
- ARPS Decline Curve Analysis
- Power BI
- DAX
- Power Query

---

## Key Outcomes

- Built well-level production forecasts across 12 wells
- Implemented ARPS parameter fitting and forecast generation
- Added R²-based model-fit diagnostics
- Created interactive production intervention scenarios
- Integrated historical production, business plans and forecast outlooks
- Built portfolio-level decline and production monitoring
- Migrated the solution from local development files to Microsoft Fabric Lakehouse
- Developed an end-to-end Fabric-to-Power-BI reporting workflow

---

## Disclaimer

This repository is a portfolio representation of the analytical solution and architecture.

Any information displayed publicly is synthetic, anonymised or recreated for demonstration purposes. No confidential client or company data, credentials or internal connection details are included.
