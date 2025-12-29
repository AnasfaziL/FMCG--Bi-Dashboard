# FMCG--Bi-Dashboard
FMCG Operations Dashboard - Client
Requirement Document
1. Project Overview
Client: TBM Consumer Products Pvt. Ltd.
Background:
TBM is an FMCG company distributing products across multiple channels and regions in
India. Management needs an Operations Dashboard that combines Sales, Inventory and
Procurement data to improve decision making at store, regional and product levels.
Analyst Role:
You are an analyst engaged by TBM. Using the provided dataset (Excel files uploaded by the
client to a shared Google Drive), build a professional, interactive Power BI report focused on
Operations, Inventory and Procurement.
2. Data Source & File Locations
The client will place source Excel files in a shared Google Drive folder and share a
downloadable link with you. Files and sheets (names must not be changed):
1. TBM_Data_2023_2025.xlsx
 - Sheet: FactSales
 - Sheet: FactInventory
 - Sheet: DimProduct
 - Sheet: DimCustomer
 - Sheet: DimStore
 - Sheet: DimDate
Guidelines:
- Expect CSV/Excel format only. If you prefer CSV, the client will provide separate CSVs with
the same sheet names.
- Maintain the original column names. Any calculated columns should be created in Power
BI (Power Query or measures) and documented.
- If you need updated data during the project, request the updated files through the client
contact below.
3. Objective & Scope
Objective:
Deliver a 3-page Power BI report (Overview, Inventory, Procurement) with interactive
visuals, slicers and exported insights. Keep calculations simple and prefer Power Query
steps or built-in aggregations; minimize DAX complexity.
Scope:
- Connect to provided Excel files and build a star-schema model in Power BI.
- Create the 10 KPIs listed in section 4 and recommended visuals in section 5.
- Provide brief documentation (one-page) explaining data sources, any transformations and
how each KPI is calculated.
4. KPIs to Deliver (Minimal/No DAX)
You must deliver the following 10 KPIs. Most of them can be created using simple
aggregations or Power Query transformations.
1. 1. Total Sales Amount
2. 2. Total Quantity Sold
3. 3. Total Received Quantity
4. 4. Average Unit Price
5. 5. Closing Stock (Current Period)
6. 6. Top 10 SKUs by Sales Volume (Pareto thinking)(80/20 rule).
7. 7. Stock Coverage Days — For a selected period: ClosingStock / (Average Daily Sales)
where Average Daily Sales = SUM(QuantitySold) / Number of days in period.
8. 8. Sell-through Rate (%) — SUM(QuantitySold) / (SUM(OpeningStock)) +
SUM(ReceivedQty)). Express as percentage; show by product or category.
9. 9. Store Fill Rate (%) — For each store: (Count of SKUs with ClosingStock > 0) / (Total
SKUs) × 100. Use a matrix or card with filter by store.
10. 10. Purchase vs Consumption Ratio (%) — SUM(ReceivedQty) / SUM(QuantitySold)
× 100. Card or gauge per category/store.
5. Suggested Visuals and Layout
Overview Page (Page 1):-
- Top row: KPI cards — Total Sales, Total Quantity, Avg Unit Price, Purchase vs
Consumption %
- Middle: Line chart (Month on Month Sales) with overlay of Received Qty as columns.
- Right: Top 10 SKUs by Sales (bar chart) and a slicer for Category and Region.
Inventory Page (Page 2):-
- KPI cards: Closing Stock, Stock Coverage Days, Sell-through Rate.
- Matrix: Store → Product → ClosingStock.
- Heatmap: Store vs Category showing closing stock levels.
Procurement Page (Page 3):-
- KPI cards: Total Received Qty, Purchase vs Consumption %.
- Bar chart: Received Qty by Supplier (simulated as Product Brand if supplier not present).
- Table: Recent receipts with Date, Product, Qty, Store.
6. Data Quality, Assumptions & Constraints
Data Quality Checks:
- Check for missing ProductKey, DateKey, StoreKey in fact tables. Report any anomalies in
the documentation.
- Ensure quantities are non-negative and dates fall within 2023-2025.
Assumptions:
- UnitPrice in DimProduct is representative of selling price; discounts already applied in
FactSales.
- Purchase data comes via FactInventory[ReceivedQty] (no separate Purchase Orders table).
Treat Brand as supplier proxy.
Constraints:
- No supplier master or PO-level dates are provided; complex procurement KPIs that need
PO-level data are out of scope.
- Keep transformations reproducible in Power Query; document every transformation step.
7. Deliverables & Timeline
Deliverables:
- Power BI .pbix file with three report pages and a cleaned data model.
- One-page calculation document describing how each KPI is obtained (short formulas or
Power Query steps)..
Suggested Timeline
- Day 0: Receive dataset (client uploads to Google Drive).
- Day 1-2: Data model & basic visuals.
- Day 3: KPI refinements and layout.
- Day 4: Documentation & final touch.
8. Client Contact & Acceptance Criteria
Acceptance Criteria:
- All 10 KPIs are present and functioning with slicers for Date, Category and Region.
- No broken relationships or missing links in the model.
- Visuals are clear, labeled and deliver business insights (short insight text for 3 major
findings).
- Documentation describes exactly how to refresh data.
