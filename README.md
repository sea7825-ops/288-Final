# LA Urban Heat & Carbon Risk Explorer
## ESPM 288 Final Project

**Author**: Qingrong (Serena) Li  
**Date**: May 2026

---

## Scientific Question
Which neighborhoods in Los Angeles face the greatest combined 
environmental burden from low vegetation cover, high pollution, 
and high electricity-based carbon emissions and where should 
green infrastructure investment be prioritized?

## Methods & Data Sources

| Layer | Data | Source | Tool |
|-------|------|--------|------|
| Vegetation (NDVI) | Sentinel-2 summer 2023 | STAC earth-search | gdalcubes |
| Redlining boundaries | HOLC 1930s maps | Source Cooperative | duckdbfs |
| Pollution burden | CalEnviroScreen 4.0 | CA OEHHA ArcGIS API | sf |
| Electricity & carbon | CEC county data 2023 | CA Energy Commission | readxl |
| AI analysis | NRP LLM service | ellm.nrp-nautilus.io | ellmer |

## Key Findings
- Grade A (historically "Best") neighborhoods have 2× higher NDVI 
  than Grade D ("Hazardous") neighborhoods
- Grade D areas show higher CalEnviroScreen pollution burden scores
- Commercial sector accounts for the highest carbon emissions 
  (2.26M MT  (2.26M M23), follo  d b  (2.26M MT  (2..89M MT  (2.26M MT  (2.26M M23), follo  d b  (2.26M MT  (2..89M urden identifies 
  priority areas for green infrastructure investment

## Repository Structure
final-project-sea7825-ops/
├── README.md
├── index.html                    # Interactive web dashboard
├── la-energy-heat.qmd            # Main analysis (Quarto)
├── la-energy-heat.html           # Rendered report
├── ellmer-analysis.R             # AI analysis script
└── data/
├── holc_pollution.geojson    # Spatial data for web map
└── ca_electricity_county.xlsx
## Tools Used
- `duckdbfs` — cloud-native remote data loading
- `gdalcubes` + `rstac` — satellite imagery processing
- `sf` — vector spatial analysis
- `mapgl` — 3D interactive mapping
- `ellmer` — AI-powered analysis via NRP LLM
- MapLibre GL JS — web map visualization
- Chart.js — electricity/carbon bar chart

## How to View
1. Open `la-energy-heat.html` for the full analysis report
2. Open `index.html` with a local server for the interactive dashboard
