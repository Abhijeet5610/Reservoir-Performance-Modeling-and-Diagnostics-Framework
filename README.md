# Reservoir-Performance-Modeling-and-Diagnostics-Framework

A Python-based reservoir engineering project that integrates classical reservoir engineering techniques to estimate hydrocarbon reserves, identify dominant reservoir drive mechanisms, optimize production performance, and forecast future production. The workflow employs dynamic PVT calculations that continuously update fluid properties as reservoir pressure declines, enabling realistic reservoir performance analysis.

---

## Overview

This project combines four fundamental reservoir engineering workflows into a single analytical framework:

- Dynamic Black Oil PVT property calculations
- Material Balance Equation (MBE) for OOIP estimation
- Nodal Analysis for production optimization
- Decline Curve Analysis (DCA) for production forecasting

Fluid properties are recalculated at every pressure step, allowing pressure-dependent reservoir behavior to be captured throughout the production life of the reservoir.

---

## Features

### Dynamic Black Oil PVT Calculator

- Bubble Point Pressure (Pb)
- Solution Gas-Oil Ratio (Rs)
- Oil Formation Volume Factor (Bo)
- Gas Formation Volume Factor (Bg)
- Gas Compressibility Factor (Z)

### Material Balance Analysis

- Havlena-Odeh Material Balance Method
- Original Oil in Place (OOIP) Estimation
- Water Influx Estimation
- Reservoir Drive Mechanism Identification
- Dynamic Drive Indices
  - Depletion Drive Index (DDI)
  - Gas Cap Drive Index (GDI)
  - Water Drive Index (WDI)
  - Compaction Drive Index (CDI)

### Nodal Analysis

- Vogel Inflow Performance Relationship (IPR)
- Darcy-Weisbach Vertical Lift Performance (VLP)
- Dynamic Operating Point Prediction
- Optimum Production Rate Estimation

### Decline Curve Analysis

- Arps Hyperbolic Decline Model
- Production Forecasting
- Remaining Reserve Estimation
- Estimated Ultimate Recovery (EUR)
- Recovery Factor Calculation

### Reservoir Validation

- Recovery Factor Validation
- Drive Mechanism Consistency Check
- Physics-Based Reservoir Sanity Audit

---

## Workflow

```
Reservoir Input Data
        │
        ▼
Read Excel Dataset
        │
        ▼
Dynamic Black Oil PVT Calculations
        │
        ▼
Material Balance Analysis
        │
        ├──► OOIP Estimation
        ├──► Water Influx Estimation
        └──► Drive Mechanism Analysis
        │
        ▼
Nodal Analysis
        │
        ▼
Operating Flow Rate Optimization
        │
        ▼
Decline Curve Analysis
        │
        ▼
Production Forecast & Ultimate Recovery
```

---

## Input Data

The project uses an Excel workbook containing two worksheets.

### Parameters Sheet

Reservoir, fluid, and well parameters including:

- API Gravity
- Gas Gravity
- Reservoir Temperature
- Initial Reservoir Pressure
- Initial Solution GOR
- Oil Compressibility
- Rock Compressibility
- Water Compressibility
- Initial Water Saturation
- Well Depth
- Productivity Index
- Tubing Diameter
- Wellhead Pressure

### Production History Sheet

Historical production data including:

- Reservoir Pressure
- Monthly Oil Production Rate
- Cumulative Oil Production
- Cumulative Gas Production
- Cumulative Water Production
- Production Time

---

## Engineering Models Implemented

### PVT Correlations

- Standing Bubble Point Correlation
- Standing Oil Formation Volume Factor Correlation
- Standing Solution Gas-Oil Ratio Correlation
- Sutton Pseudo-Critical Property Correlation
- Beggs & Brill Gas Compressibility Correlation

### Material Balance

- Havlena-Odeh Linearized Material Balance Equation
- Schilthuis Water Influx Approximation

### Inflow Performance

- Vogel IPR Model
- Productivity Index Model (Above Bubble Point)

### Production Forecasting

- Arps Hyperbolic Decline Curve Analysis

---

## Output

The workflow generates:

- Dynamic PVT Property Curves
- Oil Formation Volume Factor (Bo) vs Pressure
- Solution GOR (Rs) vs Pressure
- Gas Formation Volume Factor (Bg) vs Pressure
- Havlena-Odeh Straight Line Plot
- Dynamic Reservoir Drive Index Evolution
- Nodal Analysis (IPR-VLP) Curves
- Optimum Operating Point
- Production Decline Forecast
- Estimated Ultimate Recovery (EUR)
- Recovery Factor
- Reservoir Performance Validation Report

---

## Technologies Used

- Python
- NumPy
- Pandas
- SciPy
- Matplotlib
- OpenPyXL

---

## References

1. Standing, M. B. (1947). *A Pressure-Volume-Temperature Correlation for Mixtures of California Oils and Gases.*

2. Havlena, D., & Odeh, A. S. (1963). *The Material Balance as an Equation of a Straight Line.*

3. Vogel, J. V. (1968). *Inflow Performance Relationships for Solution-Gas Drive Wells.*

4. Arps, J. J. (1945). *Analysis of Decline Curves.*

5. Ahmed, T. *Reservoir Engineering Handbook.*

6. Craft, B. C., & Hawkins, M. *Applied Petroleum Reservoir Engineering.*



**Abhijeet Kumar**  
Petroleum Engineering  
Indian Institute of Technology (ISM) Dhanbad
