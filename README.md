# STR Hotel Performance Analysis – Property X (Jul–Dec 2023)

A Power BI dashboard benchmarking a hotel ("Property X") against a competitive set of six hotels, using STR-style KPIs to diagnose performance and recommend actions.

<img width="1310" height="399" alt="image" src="https://github.com/user-attachments/assets/c2edcd81-925f-4e77-913b-a25872e09314" />


## Business Question
Why is Property X underperforming its competitors on revenue per room, and what should the hotel do about it?

## Tools & Skills
- **Power BI Desktop** – data modelling, DAX measures, interactive report
- **Custom visuals** – Power KPI Matrix
- **Hotel analytics** – Occupancy, ADR, RevPAR, and market indices (MPI, ARI, RGI)

## Key Metrics (Jul–Dec 2023)

| KPI | Property X | Rank (of 6) |
|---|---|---|
| Occupancy | 57% | 5th |
| ADR | ~$190 | 4th |
| RevPAR | ~$111 | 4th |

| Index | Value | What it means |
|---|---|---|
| MPI (Occupancy Index) | 85% | Capturing less than its fair share of demand |
| ARI (Rate Index) | 107% | Pricing above the market |
| RGI (Revenue Index) | 103% | Slightly ahead of the market on RevPAR |

## Key Findings

**1. The problem is volume, not price.** ARI of 107% shows strong pricing power, but an MPI of 85% means the hotel is losing guests to competitors.

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

**4. Trend:** Occupancy declined from July to November, with a recovery in November–December likely tied to festive-season demand.

## Recommendations
- **Grow weekday occupancy:** corporate packages and local business tie-ups, Sunday–Thursday extended-stay bundles, and better online visibility targeting business travellers.
- **Protect weekend performance:** keep dynamic pricing and add event-based and leisure packages.
- **Improve demand capture in peak months** through targeted marketing and offers.

## Repository Contents
| File | Description |
|---|---|
| `STR_Hotel_Analysis_2023.pbix` | Power BI report (open with Power BI Desktop) |
| `docs/Property_X_Analysis_Recommendations.pdf` | Full written analysis and recommendations |
| `screenshots/` | Dashboard page previews |

## How to View
Download the `.pbix` file and open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows). If you don't have Power BI, the screenshots and PDF summarize the analysis.
