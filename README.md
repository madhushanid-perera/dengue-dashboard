# 🦟 Sri Lanka Dengue Surveillance Dashboard

An interactive Quarto dashboard for exploring weekly, district-level dengue case data across Sri Lanka (2006–2025). Built for public health analysts to understand long-term trends, seasonal patterns, geographic distribution, and outbreak behaviour of dengue nationwide.

**🔗 Live Dashboard:** [https://madhushanid-perera.github.io/dengue-dashboard/](https://madhushanid-perera.github.io/dengue-dashboard/)

---

##  About

Dengue is an endemic, strongly seasonal disease in Sri Lanka, concentrated in the populous wet-zone districts and punctuated by occasional, statistically distinct epidemic years — most notably 2017 and 2019. This dashboard brings together interactive charts, maps, and tables to surface that story directly from the data, moving from the broadest national picture down to district-level detail.

##  Dashboard Pages

| Page | What it shows |
|---|---|
| **Overview** | Headline KPIs, national weekly time series, annual totals, current year's seasonal position, and a district map |
| **Seasonality & Trends** | Recurring within-year seasonal patterns and year-on-year comparisons |
| **District & Province Analysis** | Geographic breakdown of case burden by district and province, including two browsable heatmaps |
| **Outbreak Analysis** | Epidemic threshold and anomaly detection to identify unusual or outbreak-level weeks |
| **Data Explorer** | Searchable, filterable, and exportable table of the underlying district-level weekly records |

### Key Performance Indicators
- **Total Cases (2006–2025)** — cumulative national dengue burden
- **Peak Outbreak Year** — the single worst year on record
- **Cases in Latest Year** — most recent year's total, for context against history
- **Districts Monitored** — confirms nationwide (26-district) coverage

##  Data Source

Built on the [`denguedatahub`](https://cran.r-project.org/package=denguedatahub) R package, developed by Dr. Thiyanga S. Talagala (Department of Statistics, University of Sri Jayewardenepura) with funding from the R Consortium's Infrastructure Steering Committee. For Sri Lanka, the package scrapes and cleans the Weekly Epidemiological Reports published by the Epidemiology Unit, Ministry of Health, Sri Lanka, into a tidy `srilanka_weekly_data` dataset (year, week, start/end date, district, cases).

##  Built With

- [Quarto](https://quarto.org/) dashboard format
- R — `tidyverse`, `plotly`, `leaflet`, `DT`, `denguedatahub`
- Bootswatch **cosmo** theme with custom CSS

##  Running Locally

1. Clone this repo:
   ```bash
   git clone https://github.com/madhushanid-perera/dengue-dashboard.git
   cd dengue-dashboard
   ```
2. Open `dengue_dashboard_final.qmd` in RStudio (or your preferred R environment).
3. Install any required packages if prompted (`tidyverse`, `plotly`, `leaflet`, `DT`, `denguedatahub`, etc.)
4. Render the dashboard:
   ```bash
   quarto render dengue_dashboard_final.qmd
   ```

##  Repository Structure

```
├── index.html                    # Rendered, self-contained dashboard (published via GitHub Pages)
├── dengue_dashboard_final.qmd     # Quarto source file
├── styles.css                     # Custom dashboard styling
└── Dengue_Dashboard_Report.pdf     # Full documentation & interpretation report
```

##  Author

**Madhushani Perera** B.Sc(Hons) in Statistics
Department of Statistics, Faculty of Applied Sciences
University of Sri Jayewardenepura

---

*For a full walkthrough of every chart and its epidemiological interpretation, see [`Dengue_Dashboard_Report.pdf`](./Dengue_Dashboard_Report.pdf) in this repository.*
