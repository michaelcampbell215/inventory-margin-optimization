# Inventory Margin Optimization

## **Project Overview**

**The Chaos on the Ground:** Taste of the World Cafe faced a critical disconnect between menu complexity and operational profitability. Kitchen lines were bogged down during peak hours by high-volume items that weren't actually driving revenue, while high-margin items were buried in the menu.
**The Solution:** I built an analytical "Control Tower" using advanced SQL (CTEs, Window Functions) to categorize menu efficiency. This directly exposed that the highest-volume item (Hamburger) was underperforming in revenue, providing a data-backed roadmap to restructure the menu and optimize staffing for specific peak hours.

## **Data Sources**

- **Point of Sale (POS) Transaction Logs (`fact_orders`):** Raw operational data capturing every transaction, order time, and item ID.
- **Menu Reference Data (`dim_menu_items`):** Dimensional data containing item prices, categories, and descriptions.

## **Process**

- **Data Architecture (SQL):** Engineered a robust dimensional model (Star Schema), joining operational fact tables with menu dimensions to create an environment optimized for complex analytical querying.
- **Temporal Traffic Analysis:** Deployed cron-style SQL ordering to identify specific bottleneck hours and measure exact throughput demand on the kitchen.
- **Strategic Matrix (CTE + NTILE):** Engineered automated SQL logic to classify items into 'Star', 'Puzzle', 'Workhorse', and 'Dud' categories removing manual guesswork from menu engineering.
- **Basket Analysis:** Executed self-joins on historical transaction data to map true cross-cuisine purchasing behavior.

## **Key Findings**

- **Volume vs. Value Friction:** Proved that the Hamburger (Highest Volume) was merely a 'Workhorse', failing to drive primary revenue and eating up valuable grill capacity.
- **The "Fusion Factor":** Basket analysis revealed a high frequency of customers pairing American staples with Asian sides, highlighting an untapped 49% conversion opportunity for bundled combos.
- **Operational Peaks:** Hard data confirmed that Monday, Friday, and Sunday lunch hours were the most critical throughput bottlenecks threatening service SLAs.

## **Recommendations (Operational Scripts)**

- **Feature 'Stars':** Immediately elevate the visibility of the **Korean Beef Bowl** (High Profit / High Volume) across all digital and physical menus to maximize margin capture.
- **Menu Restructuring:** Relaunch the "Italian" segment as the primary revenue puzzle piece to stimulate underperforming categories.
- **Labor Resourcing:** Restructure the front-of-house and back-of-house shift scheduling to double coverage strictly during the identified Mon/Fri/Sun lunch peaks.

## **Next Steps**

- **Combo Pipeline:** Launch designated "Fusion Combos" (e.g., Burger + Edamame) to programmatically increase average ticket size based on detected basket pairings.
- **Automated Menu Dashboard:** Connect the engineered SQL views directly into a BI tool (e.g., Tableau) to provide management with a live, self-updating matrix of menu performance.
