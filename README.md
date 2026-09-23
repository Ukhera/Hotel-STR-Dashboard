# STR Hotel Performance Analysis – Property X (Jul–Dec 2023)

A Power BI dashboard benchmarking a hotel ("Property X") against a competitive set of six hotels, using STR-style KPIs to diagnose performance and recommend actions. *Built on a sample dataset for portfolio purposes.*

<img width="1515" height="468" alt="image" src="https://github.com/user-attachments/assets/28ef908f-eeeb-4c90-9656-80cf5b7b7691" />


## Business Question
Why is Property X underperforming its competitors on revenue per room, and what should the hotel do about it?

## Tools & Skills
- **Power BI Desktop** – data modelling, DAX measures, interactive report
- **Custom visuals** – Power KPI Matrix
- **Hotel analytics** – Occupancy, ADR, RevPAR, and market indices (MPI, ARI, RGI)
- **Data validation** – identified and corrected source-data errors before reporting

## Key Metrics (Jul–Dec 2023, 184 days)

| KPI | Property X | Comp Set | Rank (of 6) |
|---|---|---|---|
| Occupancy | 57% | 68% | 5th |
| ADR | ~$190 | ~$178 | 4th |
| RevPAR | ~$111 | ~$121 | 4th |

| Index | Value | What it means |
|---|---|---|
| MPI (Occupancy Index) | 85% | Capturing 15% less than its fair share of demand |
| ARI (Rate Index) | 107% | Pricing 7% above the market |
| RGI (Revenue Index) | 91% | Trailing the market on RevPAR by 9% |

## Key Findings

**1. The problem is volume, not price.** The hotel prices 7% above the market, but captures 15% less demand, so it trails the market on revenue per room by 9%. The rate premium doesn't make up for the lost occupancy.

**2. Weekdays drive the underperformance.**

| Weekday | Property X | Comp Set |
|---|---|---|
| Occupancy | 55% | 70% |
| ADR | $186 | $179 |
| RevPAR | $103 | $126 |

Occupancy trails the comp set by 15 percentage points, which outweighs the rate premium.

**3. Weekends are a strength.**

| Weekend | Property X | Comp Set |
|---|---|---|
| Occupancy | 63% | 62% |
| ADR | $201 | $177 |
| RevPAR | $129 | $109 |

**4. Trend:** Occupancy declined from July to October, then recovered in November–December, likely tied to festive-season demand.

## Data Quality Note
Validating the source data turned up two errors:
- **28 Sep 2023:** the RGI field held 2000.0 instead of ~101.4, which inflated the period RGI from 91% to 103%.
- **10 Jul 2023:** ADR was recorded as 0 despite 63.2% occupancy and $90 RevPAR (true ADR ≈ $142).

**Note:** the dashboard file and screenshot still show the original RGI of 103%. The corrected figure of 91% is used throughout this README. The fix, to be applied in the next version of the report, is to calculate the indices as ratios of aggregates, so a single bad record can't distort the result:

```dax
RGI = DIVIDE(SUM(Master_Data[My Prop Rev PAR]), SUM(Master_Data[Comp Set Rev PAR]))
```

## Recommendations
- **Grow weekday occupancy:** corporate packages and local business tie-ups, Sunday–Thursday extended-stay bundles, and better online visibility targeting business travellers.
- **Protect weekend performance:** keep dynamic pricing and add event-based and leisure packages.
- **Improve demand capture in peak months** through targeted marketing and offers.

## Repository Contents
| File | Description |
|---|---|
| `STR Hotel_Analysis_2023.pbix` | Power BI report (open with Power BI Desktop) |
| `Property X Analysis & Recommendations.pdf` | Written analysis and recommendations |

## How to View
Download the `.pbix` file and open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows), or upload it to the Power BI Service. The screenshot above and the PDF summarize the analysis.
