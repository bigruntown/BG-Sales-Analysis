# BG Sales Analysis — Retail Chain Performance (Capstone)

A Power BI capstone project that benchmarks sales performance across a portfolio of retail shops, ranking individual stores within their competitive territory and surfacing the leaders and laggards in the chain.

## Overview

For multi-shop retail businesses, the most useful question isn't "how much did we sell?" — it's **"how is each shop performing relative to its peers, and which territories are over- or under-indexing?"**

This report builds a chain-wide performance view that lets a regional manager rank individual shops, compare them within their territory, and spot where intervention (or replication of best practice) is needed.

## Tools

- **Microsoft Power BI Desktop**
- **DAX** — for ranking and per-area normalisation measures
- **Data modelling**

## Dataset

A retail chain dataset (`Names` table) capturing:

- `ShopID` — individual shop identifier
- `Name` — shop name
- `Chain` — parent chain
- `Territory` — geographic / competitive grouping
- `Sales` — transactional sales

### KPI cards & measures

- **Total Revenue**
- **Total Annual Sales**
- **Sales Rank** — DAX rank measure ordering shops by performance
- **Annual sales per selling area** — productivity measure (sales normalised by store size)
- **Competitive Territory** — segmentation grouping shops that genuinely compete with each other

### Visuals

- **Card visuals** for the top-line KPIs
- **Clustered bar chart** ranking shops by sales
- **Column chart** for chain-level comparison
- **Line chart** showing sales over time
- **Pie chart** showing share-of-mix across chains
- **Table** with the full shop-by-shop breakdown including rank

## Key technical work

- **DAX ranking** — built a `Sales Rank` measure so the chart automatically re-ranks when the user changes filters (slicer-aware ranking is a step up from a static rank column).
- **Productivity normalisation** — `Annual sales per selling area` gives a fair comparison between large and small stores, instead of penalising small shops just for being small.
- **Competitive grouping** — the "Competitive Territory" concept reframes the dashboard from a corporate-style league table into a more operationally useful view (managers care about their territory, not the whole country).

## Screenshots

![image alt](https://github.com/bigruntown/BG-Sales-Analysis/blob/main/Screenshot.jpg?raw=true)

## How to view this project

1. Download `BG-SALES-ANALYSIS-CAPTONE-PROJECT.pbix` from this repo.
2. Open it in **Power BI Desktop** (free download from Microsoft).
3. Use the slicers to filter by chain or territory.

---

*Built as a capstone project for the Utiva Data Science program (2026).*
