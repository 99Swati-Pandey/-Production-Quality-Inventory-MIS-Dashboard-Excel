# -Production-Quality-Inventory-MIS-Dashboard-ExcelProduction, Quality & Inventory MIS Dashboard | Excel

An Excel MIS project on a simulated oral-care manufacturing plant (Manesar). It covers daily-to-monthly reporting, data accuracy checks and root-cause analysis of a quality and stock problem that the plant-level numbers did not reveal.

Note: The dataset is synthetic and created for practice. The company, plant and supplier names are illustrative and do not represent real operations.

Business problem

From July 2026 the Plant Head saw rising customer complaints about mouthwash leakage and repeated mouthwash stock-outs. The monthly MIS showed plant-level rejection under the 4% limit, so no alert was raised. Management suspected night-shift manpower. The task was to find what changed, where, and what it cost.

Dataset
Item	Detail
Records	2,000 production runs (1 run = one line, one SKU, one shift, one date)
Period	1 Apr 2026 to 30 Sep 2026
Lines	L1 Toothpaste, L2 Mouthwash, L3 Floss & Interdental, L4 Toothbrush
Shifts	A, B, C
Fields	26, covering output, rejects, defect type, packaging supplier, manpower, downtime and finished goods stock
Tools and methods
Microsoft Excel: Pivot Tables, slicers, SUMIFS, COUNTIFS, IF, lookup formulas, conditional formatting, charts
Data accuracy checks before reporting (stock reconciliation, duplicates, impossible values)
Root-cause analysis by line, shift, supervisor, supplier and defect type
Dashboard contents
KPI cards: total produced, rejection %, plan achievement %, rejection loss (INR), SKUs below reorder level
Rejection % by line and month
Rejection % by packaging supplier
Rejects by defect type and month
Mouthwash closing stock against reorder level
Slicers: Month, Line, Shift, Supplier
Key findings
Only the mouthwash line (L2) deteriorated. Rejection rose from 2.5% (Apr to Jun) to 6.5% (Jul to Sep). L1, L3 and L4 stayed at about 2.5%.
A new packaging supplier explains it. PackRight Industries was first used on 1 July, on L2 only. Its batches rejected at 10.4% against 2.4% for the other suppliers on the same line.
A new defect appeared. Cap Seal Leakage was 0 in April to June. All 65,583 units of it from July to September came from PackRight batches, and no other supplier had any.
Shift, supervisor and attendance are not the cause. PackRight runs at about 10% on every shift. Shift C looked worse only because it ran more PackRight batches. Attendance showed almost no correlation with rejection.
The plant-level rate hid it. Plant rejection was 3.4% in Jul to Sep, under the 4% limit, even though L2 more than doubled.
Stock and cost impact.
About ₹32 lakh excess rejection loss from PackRight batches in 3 months
Average mouthwash closing stock fell about 49%
20 zero-stock runs in September, with about 12,900 units of unmet demand
Recommendations
Put PackRight on hold or under supplier corrective action, and confirm the cap fault with an incoming inspection and a trial against another supplier.
Add incoming inspection of caps before they reach the bottling line.
Raise mouthwash planning and safety stock until quality recovers.
Report rejection by line, supplier and defect type, with a 3% line-level limit and low-stock alerts.
Limits of the analysis
The data shows a very strong link between PackRight packaging and the leakage, not the physical cause. That needs a physical inspection.
Lost sales are valued at manufacturing cost, so the true revenue loss is higher.
The data is synthetic and covers six months only.
Repository contents
├── Perfora_Production_MIS_Dataset.xlsx   # dataset (Data, Questions, Data_Dictionary sheets)
├── Perfora_MIS_BRD.docx                  # Business Requirements Document
├── Production_MIS_Dashboard.xlsx         # my pivots, charts and dashboard  <-- add your file name
└── README.md
Author

Swati Pandey | GitHub | LinkedIn
