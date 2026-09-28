# FreshMart Sales & Profitability Planning Model

## Project Overview

This project builds a simple **2026 sales and profitability planning model** for FreshMart.
The model uses **2025 historical performance** as the starting point and applies business assumptions to create a 2026 plan.

The main tool used is **Microsoft Excel**.

---

## Business Problem

FreshMart management already knows what happened in 2025.

The goal is to answer:

- What could sales look like in 2026?
- What could product costs look like?
- How much gross profit could the business make?
- How could labour and operating costs affect profit?
- What happens under different business scenarios?

---

## Tools Used

- Microsoft Excel
- MySQL

SQL was used only to prepare the historical data.

Excel was used for the main planning model.

---

## Dataset
Main tables used:

- `fact_transactions`
- `fact_transaction_lines`
- `fact_labour`
- `fact_operating_expenses`
- `dim_date`
- `dim_store`

The dataset contains historical performance for **2025 only**.

---

## Data Preparation

The raw data was prepared at:

**Month × Store level**

The main historical measures were:

- Net Sales
- Cost of Goods Sold (COGS)
- Labour Cost
- Operating Expenses
- Gross Profit
- Gross Margin %
- Operating Profit
- Operating Margin %

### Main calculations

**Gross Profit**

```text
Net Sales - COGS
```

**Gross Margin %**

```text
Gross Profit / Net Sales
```

**Operating Profit**

```text
Gross Profit - Labour Cost - Operating Expenses
```

**Operating Margin %**

```text
Operating Profit / Net Sales
```

---

## Planning Assumptions

The 2026 plan is based on four main assumptions:

- Sales Growth %
- COGS Inflation %
- Labour Cost Increase %
- Operating Expense Increase %

Three scenarios were created:

| Assumption | Downside | Base | Upside |
|---|---:|---:|---:|
| Sales Growth % | -2% | 3% | 6% |
| COGS Inflation % | 5% | 3% | 1% |
| Labour Cost Increase % | 6% | 4% | 3% |
| Operating Expense Increase % | 5% | 3% | 2% |

These values are **planning assumptions**, not predictions.

---

## 2026 Planning Model

The model uses 2025 performance as the baseline.

### Planned Sales

```text
2025 Sales × (1 + Sales Growth %)
```

### Planned COGS

```text
2025 COGS × (1 + Sales Growth %) × (1 + COGS Inflation %)
```

### Planned Labour Cost

```text
2025 Labour Cost × (1 + Labour Cost Increase %)
```

### Planned Operating Expenses

```text
2025 Operating Expenses × (1 + Operating Expense Increase %)
```

The model then calculates planned gross profit, operating profit and margins.

---

## Scenario Analysis

A scenario selector allows the user to choose between:

- Downside
- Base
- Upside

Changing the scenario automatically changes the 2026 plan.

A separate comparison table also shows all three scenarios side by side.

This helps management understand how changes in sales and costs could affect profitability.

---

## Workbook Structure

The workbook contains:

### `Historical_Actuals`

Shows 2025 performance by month and store.

### `Assumptions`

Contains the Downside, Base and Upside assumptions.

### `2026_Plan`

Shows the detailed 2026 sales and profitability plan.

### `Management_Summary`

Shows:

- 2025 Actual vs 2026 Base Plan
- Downside vs Base vs Upside
- Key profitability measures
- Simple charts
- Business commentary

---

## Key Measures

The final model focuses on:

- Planned Sales
- Planned COGS
- Gross Profit
- Gross Margin %
- Labour Cost
- Operating Expenses
- Operating Profit
- Operating Margin %

---

## Model Limitation

The dataset contains only **one year of historical data**.

Because of this, the project does not use advanced forecasting or claim to predict future performance.

The 2026 plan is an **assumption-driven planning model**.

The dataset is also synthetic, so some values may not fully represent the economics of a real supermarket.

---

## Project Flow

```text
2025 Historical Performance
        ↓
Planning Assumptions
        ↓
2026 Sales & Cost Plan
        ↓
Gross Profit
        ↓
Operating Profit
        ↓
Scenario Analysis
        ↓
Management Summary
```

---


## Final Purpose

The project shows how historical retail data can be turned into a simple planning model that helps management understand how changes in **sales, product costs, labour and operating expenses** can affect future profitability.
