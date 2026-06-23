# UrbanSpark Logistics — End-to-End Supply Chain Optimisation

A portfolio-level supply chain analysis project for a fictional B2B wholesale 
distributor of premium e-bike components, based in Munich, Germany.

> Fictional company. Dataset generated with AI assistance (Claude, Anthropic). 
> All analytical work conducted by the author.

## Live

- [Interactive Dashboard](https://ralenc.github.io/urbanspark_supply-chain-project)
- [Project Report (PDF)](./UrbanSpark_Report.pdf)

## What this project covers

- **ABC-XYZ segmentation** of a 38-SKU portfolio by revenue contribution 
  and demand variability
- **Route optimisation** via Log-Hub Last Mile across 5 delivery zones — 
  projected savings of ~€101,700/year identified
- **Inventory policy redesign** — safety stock, reorder points and EOQ 
  recalculated for all 38 SKUs using a differentiated (s,Q) framework 
  by ABC-XYZ segment
- **Monte Carlo simulation** (Python) projecting a 74% reduction in 
  stockout frequency (33 → ~9 events/year)
- **KPI baseline** — 18 KPIs compared As-Is vs To-Be across transport, 
  inventory and stockout dimensions

## Repository contents

| File | Description |
|---|---|
| `index.html` | Interactive analytics dashboard (live on GitHub Pages) |
| `UrbanSpark_RawData.xlsx` | Full Excel workbook — data model, ABC-XYZ, route optimisation, inventory policy, KPI sheet |
| `UrbanSpark_Report_Updated.pdf` | Full project report covering methodology, results, limitations and recommendations |
| `simulation.py` | Monte Carlo stockout simulation — runs automatically from the Excel workbook |
| `extract_data.py` | Data extraction script — reads policy parameters and demand history from Excel |
| `all_new_routes - View.png` | Log-Hub output — optimised routes across all 5 zones |
| `munich_new_routes - View.png` | Log-Hub output — optimised Munich MUC_1 and MUC_2 routes |

## Running the simulation

```bash
pip install openpyxl numpy
python simulation.py
```

Place `UrbanSpark_RawData.xlsx`, `simulation.py` and `extract_data.py` 
in the same folder. Running `simulation.py` triggers the extraction 
automatically and prints results to the terminal.

## Tools used

Microsoft Excel · Log-Hub (Last Mile) · Python (NumPy, openpyxl)
