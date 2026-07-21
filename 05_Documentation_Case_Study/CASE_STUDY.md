# Total Rewards Analytics — Case Study

**Role:** Data Analyst (solo project) &nbsp;|&nbsp; **Tools:** Excel (pivots, live formulas), Power BI &nbsp;|&nbsp; **Data:** 492-employee rewards & benefits dataset

## Problem

Two questions come up whenever a company reviews rewards spend: where is benefit cost concentrated, and is it justified — and is the gender pay gap serious enough to require a compensation fix. This project answers both from employee-level salary, benefit plan, and premium data.

## Approach

1. Cleaned and validated the raw employee dataset (outlier checks on salary via IQR, zero unresolved audit exceptions).
2. Built pivot-based analysis in Excel: headcount, salary, and premium cost cut by department, location, salary band, and gender.
3. Built a live, filterable Excel dashboard (KPI cards, charts, benchmarking table) and a matching Power BI report.
4. Controlled the raw gender pay gap for salary band to test whether it reflects unequal pay or workforce composition.

## Key Findings

**Cost is concentrated, not spread evenly.** Company-wide, 23.4% of employees are "high-cost" (monthly premium above ₹7,000). Two department×location combinations sit 8–11 points above that average:

| Department | Location | High-Cost % | Headcount | Avg Monthly Premium (₹) |
|---|---|---|---|---|
| Finance | Hyderabad | 34.5% | 29 | 5,945 |
| Sales | Gurugram | 32.0% | 25 | 6,062 |
| Operations | Hyderabad | 30.8% | 26 | 5,475 |
| Sales | Noida | 29.2% | 24 | 5,294 |
| **Company average** | — | **23.4%** | **492** | **5,250** |

**The pay gap is a representation issue, not a pay issue.** The raw, company-wide gap is 9.34% in favor of men. Once salary band is controlled for, the gap in every band falls under 3% and the direction flips — women earn more in the Mid and Lead bands, men earn more in Junior and Senior. That's normal variation, not a systemic gap.

The number that *does* matter: women make up 53% of Junior headcount but only 36% of Lead headcount — the steepest drop of any band transition. That's a promotion-pipeline pattern, not a compensation one, and it's invisible if the review stops at "is pay equal."

## Recommendations

1. **Investigate two units first** — plan mix and vendor premium rates in Finance–Hyderabad and Sales–Gurugram. Best cost-to-effort ratio: 54 employees combined, 8–11 points above benchmark.
2. **Don't adjust salary bands on equity grounds** — band-controlled gaps run in both directions within a normal range; a pay correction here would spend budget on a problem the data doesn't show.
3. **Open a separate review of the Senior → Lead promotion pattern by gender** — this is where the real equity exposure sits, and it's an HR process question, not a compensation one.
4. **Formalize a tier-to-grade policy8* — Capping Junior/Mid eligibility at Silver would cut an estimated ₹4.89L/month (~₹58.7L/year) in premium spend currently happening by default, not by policy.

## Repo Structure

- `01_Raw_Data` — source employee dataset (cleaned, validated)
- `02_Excel_Analysis` — pivot-table analysis by department, location, band, gender
- `03_Excel_Dashboard` — interactive Excel dashboard (KPI cards, filters, charts, benchmarking table)
- `04_Power_BI_Dashboard` — matching Power BI report
- `05_Documentation_Case_Study` — this write-up + one-page executive summary
