---
title: "Final Financial Audit"
subtitle: "Project ID: P1048-Nishio MY PX33 TOTO"
author: "Finance & Project Controls"
date: "22 May 2025"
toc: true
numbersections: true
---

# Executive Summary

This Final Financial Audit compares the original estimate in `project_budget.md` against realized costs in `actual_costs.md` for Project **P1048-Nishio MY PX33 TOTO**.

## Key Result

- **Budget (normalized with actual FX): RM89,777.50**
- **Actual: RM108,656.09**
- **Variance: +RM18,878.59 (+21.03%)**

## Primary Drivers of Overrun

1. **Installation Labor**: +RM16,012.50 (+500.00%)
2. **Shipment**: +RM3,243.00 (+300.28%)
3. **Travel**: +RM1,448.00 (+72.40%)

## Offsets (Underruns)

- **Pre-Sales**: -RM1,255.91 (-19.32%)
- **Tax/Custom Duty**: -RM644.00 (-19.88%)

## Audit Opinion

Costs are arithmetically consistent with provided records and FX assumptions. The project exceeded budget primarily due to **scope/time expansion in installation** and **logistics underestimation** in the planning baseline.

---

# Scope, Basis, and Methodology

## Scope

This audit covers all cost categories explicitly listed in:

- `project_budget.md` (budget estimate)
- `actual_costs.md` (final actuals)

## Currency and Normalization Basis

- Functional comparison currency: **RM**
- Applied FX for audit normalization: **USD1 = RM4.27** (same as actual cost document, dated 22 May 2025)

## Source Data Integrity Notes

- Budget document left labor totals as "TBD" pending FX.
- Actual document provided complete RM totals and category breakdown.
- For comparability, labor budget values were converted using RM4.27.

## Normalized Budget Labor Conversion

- Development labor budget: USD4,500 × 4.27 = **RM19,215.00**
- Installation labor budget: USD750 × 4.27 = **RM3,202.50**

## Financial Control Objective

Assess:

1. Arithmetic correctness
2. Budget realism vs actual execution
3. Variance concentration and control lessons

---

# Detailed Budget vs Actual Variance Analysis

## Category-Level Comparison

| Category | Budget (RM) | Actual (RM) | Variance (RM) | Variance % |
|---|---:|---:|---:|---:|
| Hardware & Material | 54,000.00 | 54,028.00 | +28.00 | +0.05% |
| Development Labor | 19,215.00 | 19,215.00 | 0.00 | 0.00% |
| Installation Labor | 3,202.50 | 19,215.00 | +16,012.50 | +500.00% |
| Pre-Sales | 6,500.00 | 5,244.09 | -1,255.91 | -19.32% |
| Travel | 2,000.00 | 3,448.00 | +1,448.00 | +72.40% |
| Shipment | 1,080.00 | 4,323.00 | +3,243.00 | +300.28% |
| Tax / Custom Duty | 3,240.00 | 2,596.00 | -644.00 | -19.88% |
| Miscellaneous | 540.00 | 587.00 | +47.00 | +8.70% |
| **TOTAL** | **89,777.50** | **108,656.09** | **+18,878.59** | **+21.03%** |

## Concentration of Total Overrun

- Installation Labor: **84.82%** of net overrun
- Shipment: **17.18%**
- Travel: **7.67%**
- Offsets from underruns (Pre-Sales, Tax) reduced net overrun by **10.63%**

## Cost Structure Shift

- Labor intensity increased significantly due to installation duration expansion.
- Logistics costs (travel + shipment) materially exceeded planning assumptions.
- Hardware cost remained effectively on budget, indicating stable procurement execution.

---

# Findings, Root Causes, and Control Assessment

## Finding A — Installation Labor Underestimated

- Budget basis: **40 hours** (5 workdays equivalent)
- Actual basis: **30 calendar days**
- Result: +RM16,012.50 variance

**Assessment:** Baseline likely did not reflect realistic field installation duration and site conditions.

## Finding B — Shipment Budget Formula Too Simplistic

- Budget basis: **2% of hardware cost = RM1,080**
- Actual shipment: **RM4,323**
- Result: +RM3,243.00

**Assessment:** Percentage proxy did not capture freight, handling, insurance, and route/site factors.

## Finding C — Travel Underestimation

- Budget: RM2,000 (4 trips × RM500)
- Actual: RM3,448
- Result: +RM1,448.00

**Assessment:** Trip count and/or per-trip costs were underestimated.

## Finding D — Positive Controls

- Hardware variance: +0.05%
- Development variance: 0.00%

**Assessment:** Procurement and core development estimation were accurate.

## Control Effectiveness Rating

- **Strong:** Development estimation, hardware procurement pricing
- **Moderate:** Tax projection, pre-sales planning
- **Weak:** Installation effort forecast, logistics modeling

## Compliance and Arithmetic Validation

Recalculations confirm:

- Category totals match provided source values.
- FX conversion applications are consistent.
- Grand total RM108,656.09 is internally consistent.

---

# Recommendations and Forward Controls

## Budgeting Improvements

1. **Installation WBS model** (mobilization, integration, testing, standby, rework allowance)
2. **Logistics costing model** using vendor lane quotes and insurance
3. **Travel matrix** by role, purpose, duration, regional rates

## Governance Improvements

1. **Stage-gate reforecasting** at award, pre-installation, and midpoint execution
2. **Variance triggers** at 15% or RM1,000 (whichever is lower)
3. **Separated contingency pools** (labor risk vs logistics volatility)

## Baseline for Similar Future Projects

- Keep current development-rate method.
- Re-baseline installation using empirical duration from this project.
- Build logistics from actual invoices and route profiles.

## Final Conclusion

Project delivery incurred a **21.03%** total cost overrun relative to normalized budget. The overrun is **primarily structural**, driven by installation and logistics planning assumptions rather than uncontrolled procurement or development effort.

## Sign-Off

| Name | Role | Signature | Date |
|---|---|---|---|
| [Name] | Finance Manager | __________ | __________ |
| [Name] | Project Manager | __________ | __________ |
| [Name] | Internal Auditor | __________ | __________ |

---

# Appendix A — Calculation Detail

## A1. Budget Total (Normalized to RM)

- Hardware: RM54,000.00
- Development: USD4,500 × 4.27 = RM19,215.00
- Installation: USD750 × 4.27 = RM3,202.50
- Pre-Sales: RM6,500.00
- Travel: RM2,000.00
- Shipment: RM1,080.00
- Tax: RM3,240.00
- Misc: RM540.00

**Total Budget = RM89,777.50**

## A2. Actual Total

Per `actual_costs.md`:

- Development: RM19,215.00
- Installation: RM19,215.00
- Pre-Sales: RM5,244.09
- Hardware: RM54,028.00
- Travel: RM3,448.00
- Shipment: RM4,323.00
- Tax: RM2,596.00
- Misc: RM587.00

**Total Actual = RM108,656.09**

## A3. Net Variance

**RM108,656.09 − RM89,777.50 = RM18,878.59 (+21.03%)**