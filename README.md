
# EV India Market Segmentation & Geographic Analytics

Data-driven analysis of India’s Electric Vehicle (EV) market using state-wise sales data, geographic segmentation, customer personas, and strategic recommendations for product and pricing decisions.

---

## 🚀 Overview

This repository contains an end-to-end analytics workflow built on real-world Indian EV registration data (2014–2023).  
The goal is to help an EV manufacturer answer two core business questions:

1. **What type of EV should the company produce?**  
2. **Who are the target customers, and where are they located geographically?**

The project combines **data engineering**, **segmentation modeling**, and **geospatial visualizations** to produce a consulting-grade market report and dashboards.

---

## ✨ Key Features

- **Cleaned, Structured EV Dataset**
  - State-wise, month-wise EV registrations (2014–2023)
  - Breakdown by `Vehicle_Class`, `Vehicle_Category`, and `Vehicle_Type`
  - Ready-to-use CSV and notebook-friendly format

- **Geographic Segmentation**
  - State-level EV sales ranking and market share
  - Tiering of states into **Leaders / Emerging / Growth / Early Adopters**
  - Cluster definitions based on sales volume and product mix

- **Product-Market Fit Insights**
  - Identification of **E-Rickshaw dominant states** vs **2W personal mobility states**
  - State-wise recommended product strategy (e.g., Low-speed E-Rickshaw vs Premium 2W)

- **Customer & Pricing Strategy**
  - Target customer personas by state (e.g., gig workers, IT professionals)
  - High-level pricing corridors for:
    - E-Rickshaws in Uttar Pradesh (B2B / gig economy)
    - Premium 2-wheelers in Karnataka (urban professionals)

- **Geospatial Visualizations**
  - India choropleth maps (EV sales & market share by state)
  - Tier-based market segmentation map
  - Bubble map of sales volume by state
  - (Optional) Animated time-lapse map of EV adoption over years

- **Presentation-Ready Assets**
  - High-resolution plots and maps (PNG)
  - CSV exports for segmentation summaries
  - A structured Jupyter Notebook for reproducible analysis

---



---

## 🧮 Segmentation Methods Implemented

The current version of the project includes the following segmentation layers:

- **1. Geographic Segmentation (Core)**
  - EV sales and market share by state
  - Top 10 states by volume
  - Leader / Emerging / Growth / Early Adopter tiers

- **2. Product-Based Segmentation**
  - Dominant `Vehicle_Category` and `Vehicle_Type` per state
  - E-Rickshaw vs 2W vs 4W vs Bus vs Others
  - Product-market fit recommendations by state

- **3. Cluster-Based Segmentation**
  - **Tier 1 – EV Leaders:** e.g., Uttar Pradesh, Maharashtra, Karnataka  
  - **Tier 2 – Emerging Markets:** e.g., Bihar, Delhi, Rajasthan, Kerala, Tamil Nadu  
  - **Tier 3 – Growth Markets:** e.g., Gujarat, Madhya Pradesh, Odisha, Assam, West Bengal  
  - **Tier 4 – Early Adopters:** e.g., Jharkhand, Punjab, Haryana, Chhattisgarh, Uttarakhand  

- **4. Customer Persona Mapping**
  - Gig workers and shared mobility operators (E-Rickshaw-heavy states)
  - Tech-savvy, higher-income urban buyers (premium 2W states)
  - Mixed urban–rural, cost-conscious buyers (growth markets)

- **5. Pricing & Strategy Layer**
  - Suggested price bands and financing concepts for:
    - Low-speed E-Rickshaw (UP and similar markets)
    - Premium electric scooters (Karnataka and similar markets)
  - Trade-off analysis: **adoption vs profitability**

---

## 🗺️ Geographic Visualizations

The repository includes Python utilities and notebooks to generate the following visuals:

- **India EV Sales Choropleth**
  - Color intensity = total EV sales or market share by state
- **Tier-Based Segmentation Map**
  - Distinct colors for Tier 1 / Tier 2 / Tier 3 / Tier 4 states
- **Bubble Map**
  - Bubble size ∝ EV sales volume; bubble color ∝ market share
- **Product-Market Fit Map**
  - Each state colored by its dominant vehicle category (2W / 3W / 4W / Bus / Others)
- **Optional Animated Map**
  - Time-lapse of EV adoption across states (e.g., 2018–2023)

All interactive maps are exported as `.html` files that can be opened directly in a browser and embedded into presentations.

---

## 🛠️ Tech Stack

- **Language:** Python 3.x  
- **Core Libraries:**
  - `pandas`, `numpy` – data wrangling
  - `matplotlib`, `seaborn` – static charts
  - `plotly` (express & graph_objects) – interactive and geospatial visuals
  - `scikit-learn` (optional) – clustering / advanced segmentation
- **Environment:** Jupyter Notebook / JupyterLab

---

## ⚙️ Getting Started

### 1. Clone the Repository

```
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Create and Activate a Virtual Environment (Recommended)

```
python -m venv .venv
source .venv/bin/activate      # macOS / Linux
# or
.venv\Scripts\activate         # Windows
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

### 4. Place the Dataset

- Download / export the EV dataset as a CSV (e.g. `Ev_sales_India-Sheet1-A1:H96846-v1.csv`).
- Place it under `data/raw/` or update the path in the notebook / scripts.

---

## 📘 How to Run the Analysis

### Option A: Jupyter Notebook (Recommended)

1. Launch Jupyter:

   ```
   jupyter notebook
   ```

2. Open:

   ```
   notebooks/EV_Geographic_Segmentation.ipynb
   ```

3. Run cells sequentially:
   - **Load & Clean Data**
   - **Yearly Trend Analysis**
   - **Top 10 States & Market Share**
   - **Geographic Segmentation & Tiers**
   - **Customer Personas & Product Strategy**
   - **Map Visualizations (India Choropleth / Bubbles / Product Fit)**

### Option B: Python Scripts

If you modularize logic into `src/`:

```
python src/data_preprocessing.py
python src/segmentation_geography.py
python src/customer_personas.py
python src/geo_visualizations.py
```

Each script can write intermediate CSVs and charts into `data/processed/` and `visuals/`.

---

## 📊 Example Outputs

Some of the key artifacts generated by this project:

- `geographic_segmentation_market_share.csv`  
  – State-wise total EV sales and market share

- `state_wise_detailed_profiles.csv`  
  – Top states with recommended products and target customer segments

- `geographic_cluster_segmentation.csv`  
  – Tier 1 / 2 / 3 / 4 cluster definitions

- `india_market_share_map_highres.png`  
  – Publication-ready India map for slide decks

- `india_ev_sales_map.html` / `india_product_map.html`  
  – Fully interactive web maps

---

## 🧭 Use Cases

This project is useful for:

- **EV OEMs / Startups:**  
  Market entry and product portfolio planning for India

- **Consulting / Strategy Teams:**  
  Quick-turnaround but data-backed segmentation for client pitches

- **Students / Researchers:**  
  Case study in **applied data analytics + business strategy** on real EV data

- **Data Science Portfolios:**  
  Showcasing skills across data cleaning, EDA, segmentation, and geospatial analytics  
  (Structuring the README and notebook following professional guidelines helps here [web:32].)

---

## 🗺️ Roadmap / Future Enhancements

- Add **time-based segmentation** (growth phases by state)
- Add **K-Means clustering** for multi-dimensional state profiles
- Integrate **demographic & income data** from Indian census
- Build a lightweight **Streamlit / Dash app** for interactive exploration
- Add **unit tests** for core data transformation functions
- Dockerize the environment for reproducible deployment

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository  
2. Create a feature branch: `git checkout -b feature/your-feature-name`  
3. Commit changes: `git commit -m "Add some feature"`  
4. Push to the branch: `git push origin feature/your-feature-name`  
5. Open a Pull Request










[7](https://www.daytona.io/dotfiles/how-to-write-4000-stars-github-readme-for-your-project)
[8](https://gprm.itsvg.in)
[9](https://www.reddit.com/r/programming/comments/l0mgcy/github_readme_templates_creating_a_good_readme_is/)
