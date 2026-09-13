# Marketing Campaign Performance and Budget Recommendations

An Excel portfolio project evaluating February 2021 marketing campaign performance and exploring an illustrative budget reallocation.

## Business question

Which campaigns warrant budget review, where does conversion performance weaken, and what should be verified before changing advertising spend?

## Results at a glance

| Measure | February 2021 result |
| --- | ---: |
| Advertising spend | 30,590,879.82 |
| Recorded revenue | 42,889,366.00 |
| Orders | 8,043 |
| Overall ROAS | 1.40 |

Currency was not verified; amounts retain the dataset’s original units. ROAS measures recorded revenue per unit of advertising spend, not profitability.

## Key findings

- **Campaign returns varied substantially.** `youtube_blogger` had the highest ROAS at 3.77; `facebook_lal` had the lowest at 0.11. Five of 11 campaigns recorded revenue below advertising spend.
- **Social warranted particular attention.** It received the largest spending allocation, 13.80 million, but had the lowest category ROAS, 0.86.
- **The larger funnel gap was after lead generation.** Social’s lead-to-order rate was 8.40%, compared with influencer’s 17.79%. Their click-to-lead rates were closer: 2.09% and 2.26%.
- **Cheap clicks did not necessarily produce strong returns.** `instagram_tier2` had the lowest CPC, 2.09, but a lead-to-order rate of 3.02% and ROAS of 0.63.
- **Daily comparisons reflected both returns and spending mix.** Overall ROAS was 1.11 on February 10 and 1.95 on February 26. Influencer’s ROAS and share of daily spending were both higher on February 26; this does not prove that reallocating budget would reproduce the improvement.

## Illustrative budget scenario

The workbook models a 10% reduction in `facebook_lal` spending and a 5% increase in `youtube_blogger`, with other campaign allocations unchanged.

| Scenario result | Amount |
| --- | ---: |
| Original budget ceiling | 30,590,879.82 |
| Proposed campaign spending | 30,529,582.72 |
| Unallocated reserve | 61,297.10 |

This is a proposed test scenario, not an implemented or optimized allocation. Any action depends on verifying attribution, conversion delays, campaign objectives, contribution margins, and capacity. No realized business impact is claimed.

## Data and methods

**Source:** [Digital Marketing Metrics & KPIs to Measure — Kaggle](https://www.kaggle.com/datasets/sinderpreet/analyze-the-marketing-spending).

The dataset contains 308 campaign-day records across 11 campaigns and four categories, covering February 1–28, 2021. Fields include impressions, advertising spend, clicks, leads, orders, and revenue.

Work completed in Microsoft Excel:

- Standardized campaign names with `LOWER()` and `TRIM()` and converted dates with `DATEVALUE()`.
- Checked missing values, negative values, duplicate campaign-date combinations, integer counts, and funnel consistency. Retained valid zero-order and zero-revenue records.
- Investigated unusual impression and spending values without deleting unconfirmed anomalies.
- Used PivotTables to compare campaigns, categories, dates, and selected campaign-day results.
- Calculated ROAS, CTR, CPC, CPM, CPL, conversion rates, cost per order, and average order value from the relevant totals.
- Used `XLOOKUP` and `GETPIVOTDATA` to support dashboard and scenario references.
- Built campaign ROAS, category spending, and daily ROAS charts, including a monthly ROAS reference line.
- Built contribution-margin scenarios, budget-change inputs, an unallocated reserve calculation, and an overall budget flag.

Overall ROAS is **total revenue ÷ total advertising spend**, rather than a simple average of campaign or daily ROAS.

## Files and reading order

| File | Purpose |
| --- | --- |
| `Marketing_Dashboard_February_2021.pdf` | Start here for the one-page visual overview. |
| `Marketing Campaign Performance and Budget Recommendations.pdf` | Read the findings, definitions, recommendations, and limitations. |
| `Marketing_1.xlsx` | Inspect the underlying data, calculations, PivotTables, dashboard, and budget scenario. |
| `README.md` | Project introduction and navigation guide. |

These are the companion file names; place the files alongside this README when packaging the portfolio.

In the workbook, begin with `Dashboard`, then inspect `Campaign-summary`, `Category_analysis`, and `Daily_analysis`. Campaign-specific worksheets provide deeper investigations. `buget_scenarios` contains the illustrative allocation and margin assumptions; `Cleaned_data` contains the prepared records. The worksheet name `buget_scenarios` is retained as it appears in the workbook.

For the saved February analysis, keep the campaign summary filter set to **All**. Some supporting formulas refer to fixed PivotTable ranges; check their references after changing filters, expanding the dataset, or altering PivotTable layouts. This workbook is a February case study, not an automated reporting pipeline.

## Limitations

- One month of observations does not establish seasonal or long-term performance.
- The dataset’s original collection process, currency, and business context were not independently verified.
- Revenue attribution does not establish incremental revenue caused by advertising.
- Aggregate daily funnel counts do not link individual leads to subsequent orders or resolve conversion delays.
- Actual variable and fixed costs were unavailable, so profitability cannot be established and contribution margins are hypothetical.
- Unusually high impression and spending values remain unverified.
- The workbook’s daily order benchmark uses the rounded monthly rate of 3.02%; the report’s benchmark example uses the full-precision rate. This small rounding difference does not change the conclusions, but the two are not an exact numerical reconciliation.
- Proposed budget changes were not implemented or experimentally tested, and historical ROAS does not guarantee returns at higher spending.

## Tools and assistance

Microsoft Excel was used for data preparation, formulas, PivotTables, scenario analysis, and dashboard charts. AI assistance supported step-by-step learning, troubleshooting, report drafting, and review. The workbook was developed through hands-on Excel work; the recommendations are analytical proposals rather than measured business outcomes.
