# Recruitment Funnel Analysis (SQL + Power BI)

## Business Question
Where are candidates dropping off in the hiring process, and which departments, roles, or sourcing channels need improvement?

## Dashboard

![Dashboard](dashboard_screenshot.png)

Interactive Power BI dashboard tracking the full hiring funnel from application to hire, with breakdowns by department and sourcing channel.

## Dataset
`recruitment_funnel.csv` — 6,000 synthetic candidate records spanning Jan 2024–Dec 2025, modeled on realistic recruitment funnel patterns. Each record tracks a candidate through five stages: **Applied → Screened → Interviewed → Offered → Hired**, across 7 departments, 20 roles, and 6 sourcing channels.

*Note: This is a synthetic dataset built to reflect realistic hiring funnel dynamics. This is standard practice for a demonstration project.*

## Files
- `recruitment_funnel.csv` — raw dataset
- `recruitment_funnel.db` — SQLite database (same data, for running SQL queries directly)
- `analysis_queries.sql` — 10 SQL queries covering funnel conversion, drop-off analysis, source effectiveness, time-to-fill, and department/role breakdowns
- `generate_data.py` — script that generated the dataset
- `dashboard.png` — Power BI dashboard screenshot

## Key Findings

1. **Overall funnel:** Of 6,000 applicants, 3,342 were screened, 1,667 were interviewed, 677 received an offer, and 583 were hired — a 9.7% overall applied-to-hire rate.

2. **Engineering has a sharp bottleneck at Screened → Interviewed:** only 31.9% of screened Engineering candidates get an interview, compared to 53.0% across all other departments combined.

3. **Referrals dramatically outperform other sourcing channels:** 17.4% of referred candidates get hired, compared to just 3.0% for Job Board leads — nearly a 6x difference.

4. **Engineering also has the highest offer-decline rate (16.7%)**, compounding its hiring difficulty at two separate stages.

5. **Average time-to-hire is 24.5 days**, with Screened → Interviewed taking the longest at 8.6 days on average.

## Recommendations
- Investigate Engineering's screening process — the drop-off is disproportionate and worth a root-cause review.
- Shift more sourcing budget/effort toward referrals given their outsized conversion rate.
- Review Engineering's offer process — a 16.7% decline rate alongside a low interview rate suggests candidates may be losing interest before an offer arrives.

## Tools Used
SQL (SQLite) · Power BI · Python (dataset generation)
