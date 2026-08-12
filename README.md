# UK Housing Affordability & Unemployment Dashboard

An interactive geospatial dashboard analysing housing affordability and labour market conditions across English local authorities.

## Live Dashboard

[View the dashboard](https://ayshazia14.github.io/uk-housing-dashboard/dashboard.html)

## Project Overview

This project investigates the spatial distribution of two key dimensions of economic inequality in England:

- **Housing affordability** — measured as the house price-to-income ratio at local authority level
- **Labour market stress** — measured by model-based unemployment rates

The analysis reveals a persistent spatial decoupling: housing unaffordability is concentrated in London and the South East, while unemployment hotspots cluster in former industrial areas of the North and coastal periphery.

## Repository Contents

```
dashboard.html   # Self-contained interactive dashboard (all dependencies embedded)
Assignment_2.ipynb  # Source notebook with full analysis and write-up
```

## Data Sources

| Dataset | Source | Coverage |
|---|---|---|
| Median gross annual pay | ONS ASHE Table 8.7a (2025 provisional) | English local authorities |
| Unemployment rate | ONS Model-Based Unemployment Estimates (Aug 2022) | English local authorities |
| House prices | HM Land Registry UK HPI full file (2024) | English local authorities, 2010–2023 |
| Local authority boundaries | ONS Open Geography Portal (2025) | England |

## Dashboard Features

- **Choropleth map** — spatial distribution of any selected metric, with ESRI Ocean basemap and CartoDB label overlay
- **Year selector** — explore house price and affordability trends from 2019–2023
- **Metric selector** — switch between median house price, affordability ratio, median income, and unemployment rate
- **Ranking chart** — top/bottom N local authorities for the selected metric and year

## Requirements (to run the notebook)

```
geopandas
pandas
numpy
matplotlib
contextily
bokeh
panel
openpyxl
xlrd
```

Install with:

```bash
pip install geopandas pandas numpy matplotlib contextily bokeh panel openpyxl xlrd
```

## Note on Unemployment Data

The model-based unemployment estimates represent a single 2022 snapshot. The year selector does not affect the unemployment rate layer — a longitudinal unemployment series would be required for fully time-comparative analysis.

## References

- Beatty, C. and Fothergill, S. (2016) *The Uneven Impact of Welfare Reform*. Sheffield Hallam University.
- Barker, K. (2004) *Review of Housing Supply*. HM Treasury.
- McCann, P. (2016) *The UK Regional–National Economic Problem*. Routledge.
- ONS (2024) Annual Survey of Hours and Earnings (ASHE).
- Rey, S.J., Arribas-Bel, D. and Wolf, L.J. (2020) *Geographic Data Science with Python*.
- Szumilo, N. (2019) 'The geography of housing affordability in England', *Journal of European Real Estate Research*, 12(2).
