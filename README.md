# Netflix-Dataset-AnalystLab Project 2
 This dataset contains Netflix movies and TV shows, Show id, type, title, director, cast, country, date added, release year, rating, duration, listed-in and description.
# Netflix Dataset

## Dataset Understanding

## Data Cleaning

## Exploratory Data Analysis

## Visualizations

## Insights
# ONE-PAGE SUMMARY REPORT: NETFLIX CATALOG EXPLORATORY ANALYSIS
**Project Title:** End-to-End Data Engineering and Exploratory Data Analysis Pipeline (Netflix)  
**Analyst:** Esther Ayodele  
**Date:** June 8, 2026  

---

### 1. Data Cleaning and Validation Challenges Encountered
* **Structural Row Realignment:** Identified data parsing corruptions where extensive descriptive string values from fields like director and cast spilled downstream into the core maturity ratings column. This anomaly artificially pushed valid running duration metrics out of alignment. These instances were programmatically isolated and re-mapped back to their proper relative schema positions.
* **Categorical Missing Value Imputation:** Addressed substantial structural null data footprints within critical dimensions including director, cast, and country. Rather than utilizing aggressive row-deletion protocols—which would artificially strip out historical macro trends—missing nodes were handled using standardized categorical placeholders (Unknown Country and Unknown Director). This validation loop directly preserved over 800 records visually trackable in final global production volume models.
* **Metadata Deduplication:** Evaluated catalog instances for system replication. Redundant metadata structures were permanently removed using automated deduplication libraries to guarantee an unskewed historical catalog frequency analysis.

---

### 2. Key EDA Findings and Top Portfolio Insights
* **Insight 1 (Format Asymmetry):** The platform exhibits a massive structural dominance of Movie assets over episodic TV Show assets. The catalog contains over 6,000 unique Movie records compared against roughly 2,500 TV Show offerings, exposing a baseline content licensing layout centered primarily on single-sitting subscriber media.
* **Insight 3 (Adult Demographic Target Mapping):** Content asset alignment targets mature demographics. The TV-MA maturity tier comprises the single largest footprint representing 42.7% of the core ratings mix. When combined with the TV-14 market share of 28.7%, mature audiences control a combined 71.4% of total catalog space, while traditional family formats like TV-PG fill minor secondary slots (11.5%).
* **Insight 4 (Acquisition Cycle Pivots):** Aggressive programmatic catalog scaling experienced an exponential boom phase starting in 2015, culminating in an all-time annual acquisition high of over 2,000 items added during 2019. The post-2019 lifecycle shows a sharp corrective stabilization downward to roughly 1,500 entries by 2021, capturing a corporate pivot toward strategic budget curation and quality-first selection.
* **Insight 5 (Contemporary Catalog Bias):** Historical release distribution modeling demonstrates an extreme left-skewed curve. Asset frequencies remain uniformly flat between 1980 and 2010 before reaching a dramatic volume spike centered tightly upon the 2017–2018 vintage (with over 1,500 movies), showcasing a clear commercial preference for contemporary content assets over deep legacy films.
