# Inventory Margin Optimization
#### Solving the "Volume vs. Value" Friction

[![SQL](https://img.shields.io/badge/SQL-Advanced_CTEs-4479A1.svg)](https://www.mysql.com/)
[![Analysis](https://img.shields.io/badge/Methodology-Menu_Engineering-blue.svg)](https://en.wikipedia.org/wiki/Menu_engineering)

> [!IMPORTANT]
> **Executive Summary:** This project optimizes the product mix of a high-volume hospitality operation. By engineering a SQL-driven analytical engine (using CTEs and NTILE), we identified that the highest-volume item (Hamburger) was actually a low-margin "Workhorse" causing critical kitchen bottlenecks at peak hours.

---

## Project Overview

Taste of the World Cafe faced a critical disconnect between menu complexity and operational profitability. Kitchen lines were bogged down during peak hours by high-volume items that weren't driving primary revenue, while high-margin "Stars" were buried in the menu.

**The Solution:** A data-driven Gross Margin ROI (GMROI) model that optimizes both staffing and product visibility for peak throughput.

**Description:** We executed a strategic matrix analysis using advanced SQL to categorize menu efficiency and engineer targeted product mixes. 

**Objective:** Transition from anecdotal menu management to a mathematical GMROI model to boost profitability and clear operational bottlenecks.

## Data Sources

1. **Primary Datasets:** Historical transactional data containing item volume and timestamp records.
2. **Additional Data:** Financial variables including Unit Cost, Selling Price, and Gross Margin per item.

## Process

*   Quantified baseline GMROI to measure profit generated per inventory dollar.
*   Isolated Product Contribution Margin to identify true net profit after COGS.
*   Analyzed Temporal Throughput Demand to identify specific "Bottleneck Hours" exceeding kitchen capacity.
*   Executed Market Basket Analysis via self-joins to identify untapped combo opportunities.

## Technical Pivot

**From Anecdotal Reporting to Strategic Matrix (SQL CTEs & NTILE)**
Initially, menu decisions were made using simple volume reports, ignoring the cost of goods and operational strain.
*   **The Change:** We engineered automated SQL logic using advanced CTEs and the NTILE window function.
*   **The Result:** This classified 100+ items into 'Stars', 'Puzzles', 'Workhorses', and 'Duds', revealing the "Hamburger Gap" where the highest-volume item ate up 25% of grill capacity but drove minimal net profit.

**From Solo Items to Combo Pipelines**
The system previously treated every order as an independent item.
*   **The Change:** We built Market Basket Analysis logic using self-joins on historical transaction data.
*   **The Result:** Discovered a 49% untapped conversion opportunity for "American + Asian" bundled combos, allowing us to programmatically build combo packages.

## Key Insights

*   **Volume Does Not Equal Value:** The highest-selling item was actually a bottleneck. It monopolized the grill during peak rushes but yielded a low GMROI.
*   **Hidden Star Performers:** The Korean Beef Bowl had exceptional profitability and high volume but lacked marketing visibility.
*   **Natural Bundling:** Customers organically paired certain American and Asian items, but the menu failed to monetize this behavior via combo pricing.

## Recommendations

*   **Margin-First Menu visibility:** Elevate the Korean Beef Bowl to premium menu placement to capitalize on its high GMROI.
*   **Launch Fusion Combos:** Target the natural 49% pairing rate by explicitly bundling the Burger with Edamame to drive up average ticket size.
*   **Shift Peak Volume:** Restructure the Italian segment to shift demand away from the over-burdened grill stations during peak hours.

## Next Steps & Action Plan

*   **Deploy Staffing Alignment:** Restructure shift schedules to double coverage strictly during identified peak bottleneck periods.
*   **Live BI Dashboard Integration:** Connect the engineered SQL views into a live BI dashboard for real-time tracking of the Star/Dud matrix.
*   **Continuous Margin Tracking:** Establish a monthly automated review to proactively adjust menu placement before ingredient cost spikes erode margins.
