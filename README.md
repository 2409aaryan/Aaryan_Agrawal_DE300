# DE300 HW 1 — Aircraft Inventory (2006‑2023)

This repo contains a single Jupyter/Colab notebook (`DE300_HW1.ipynb`) plus the raw data archive (`T_F41SCHEDULE_B43.zip`).  
Follow the steps below to execute the notebook and reproduce the expected results.

---

## How to run the code

### Option A — Google Colab (fastest / no local setup)

1. Click **`DE300_HW1.ipynb`** in this repo, then the **“Open in Colab”** button.  
   *(If you don’t see that button, open <https://colab.research.google.com/> → **File ▸ Open Notebook ▸ GitHub** and paste this repo URL.)*
2. In Colab, run **Runtime ▸ Run all**.  
   Colab will prompt you to **connect to a runtime**; accept the default.
3. When the first code cell asks for the data file, upload the supplied ZIP (`T_F41SCHEDULE_B43.zip`) to the Colab file‑browser pane.  
   No path editing is required—the notebook is coded to detect the file automatically.

Run time: ≈ 60 seconds on the free Colab CPU runtime.

---


## Expected outputs

| Check‑point                               | What you should see when the notebook finishes |
|-------------------------------------------|-------------------------------------------------|
| **Missing‑audit**                         | `Remaining missing in 'CARRIER_imputed': 0`     |
| **Numeric imputation summary**            | `Missing after median imputation:` **all zeros**|
| **Final cleaned dataset size**            | `Final inventory rows x columns: (101316, 17)`  |
| **Box‑Cox λ values**                      | `NUMBER_OF_SEATS → 0.584` • `CAPACITY_IN_POUNDS → 0.300` |
| **Skewness after Box‑Cox**                | `NUMBER_OF_SEATS_BOXCOX skew = ‑0.53` <br> `CAPACITY_IN_POUNDS_BOXCOX skew = 0.19` |
| **SIZE distribution print‑out**           | `SMALL 19657`  `MEDIUM 30902`  `LARGE 25326`  `XLARGE 25431` |
| **Figures generated (auto‑displayed)**    | • Histogram: `NUMBER_OF_SEATS` (before) <br> • Histogram: `CAPACITY_IN_POUNDS` (before) <br> • Histogram: `NUMBER_OF_SEATS_BOXCOX` (after) <br> • Histogram: `CAPACITY_IN_POUNDS_BOXCOX` (after) <br> • Bar chart: `OPERATING_STATUS` proportions by `SIZE` <br> • Bar chart: `AIRCRAFT_STATUS` proportions by `SIZE` |


