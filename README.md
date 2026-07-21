# Total Rewards Analytics Dashboard

A rewards, benefits, and pay-equity analysis of a 492-employee dataset — built in Excel and Power BI, with a written case study.

**Start here:** [`05_Documentation_Case_Study/CASE_STUDY.md`](./05_Documentation_Case_Study/CASE_STUDY.md)

## Structure

| Folder | Contents |
|---|---|
| `01_Raw_Data` | `employee_data.csv` — cleaned source data (492 rows, 13 fields) |
| `02_Excel_Analysis` | Pivot-based analysis by department, location, salary band, gender |
| `03_Excel_Dashboard` | Interactive Excel dashboard — KPI cards, filters, charts, benchmarking table |
| `04_Power_BI_Dashboard` | Power BI (`.pbix`) version of the same dashboard |
| `05_Documentation_Case_Study` | Case study write-up + one-page executive summary |

## Note on the Excel files in `02` and `03`

These were split out of the original combined workbook using an automated tool, which flattens formulas and pivot tables to static values on save (a known limitation of scripted Excel editing) — the numbers and charts are correct, but the sheets are no longer live/refreshable inside these files. If you want to keep full pivot/formula interactivity, the safest path is to re-do this split yourself in Excel directly: open the original workbook, right-click each tab → **Move or Copy → Create a copy** into a new file, then delete the tabs you don't want in that copy. Excel preserves pivot caches and formulas natively when you do it this way; scripted tools generally don't.
