# EPL Trends Analysis (2020/21 → 2024/25 + 2025/26 start)

## 📌 Project Overview
This project analyzes **changes in the English Premier League (EPL)** across the seasons **2020/21 → 2024/25** and compares them with the start of **2025/26**.  
Focus areas:
- Goals, xG, xA, and shot quality
- Passing and build-up styles (short vs long, GK distribution, throw-ins)
- Pressing intensity (PPDA)
- Team style clusters and unexpected trends

The final outcome will include:
- **Jupyter Notebooks** with code and analysis
- **Visualizations** (trends, heatmaps, pass maps, clusters)
- **Blog article** (published on tribuna.ua)

---

## 📂 Repository Structure
```
epl-trends-analysis/
├── data/         # Raw and processed data (CSV/JSON/Parquet)
│   └── .gitkeep
├── notebooks/    # Jupyter notebooks for analysis
│   └── .gitkeep
├── src/          # Python scripts for data collection and cleaning
│   └── .gitkeep
├── reports/      # Final visualizations, charts, and results
│   └── .gitkeep
├── README.md     # Project description and documentation
└── requirements.txt
```

---

## ⚙️ Setup
1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd epl-trends-analysis
   ```

2. Create and activate virtual environment (recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Mac/Linux
   venv\Scripts\activate     # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## 📊 Analysis Plan
1. **Data Collection**
   - FBref (team/player stats via `pandas.read_html`)
   - Understat (shot-level xG data via API/scraper)
   - StatsBomb Open Data (event-level: passes, GK distribution, pressing)
   - Derived metrics: G/90, xG/90, xG per shot, PPDA

2. **Data Cleaning & Preparation**
   - Standardize team names, match IDs, dates
   - Create season-level and matchweek-level datasets
   - Store in `data/processed/`

3. **Analysis**
   - Descriptive: goals, xG, pressing intensity trends
   - Comparative: season-to-season differences
   - Exploratory: team style clusters
   - Modeling: factors influencing goals/xG

4. **Visualization**
   - Line plots of G/90, xG/90, PPDA
   - Shot maps and pass networks
   - GK distribution (short vs long)
   - Style clusters (scatter/PCA)

5. **Reporting**
   - Jupyter notebooks with cleaned results
   - Final article for tribuna.ua with insights and visuals

---

## 🛠 Tools & Libraries
- **Python:** pandas, numpy, matplotlib, seaborn, plotly
- **Web scraping/API:** requests, BeautifulSoup, aiohttp, understatapi
- **Football data:** statsbombpy
- **Modeling/EDA:** scikit-learn

---
