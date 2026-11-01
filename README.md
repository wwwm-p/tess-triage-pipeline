# tess-triage-pipeline# 
TESS Automated Target Triage & Prioritization Pipeline
An automated data-engineering framework designed to query NASA's MAST and ExoFOP databases for Transiting Exoplanet Survey Satellite (TESS) objects of interest (TOIs), automatically filter candidate metadata, and categorize targets into four distinct scientific priority tiers.

## Overview
As space telescopes generate vast datasets, automated triage becomes critical for efficient target selection. This repository contains a modular Python pipeline that ingests TESS Candidate data, cross-references multi-planet multiplicity flags, evaluates TFOPWG dispositions, and assigns target priority tiers ranging from confirmed literature targets (Tier 1) to false positives (Tier 4).

## Features
- **Automated Data Ingestion:** Connects to ExoFOP / MAST catalog metadata for TESS candidates.
- **Multi-Planet Multiplicity Detection:** Flags targets residing in multi-candidate host star systems.
- **4-Tier Priority Classification:** 
  - **Tier 1:** Confirmed Planets / Literature Ready
  - **Tier 2:** High-Priority Multi-Planet Candidates
  - **Tier 3:** Single Candidate (Requires Manual DV Report Review)
  - **Tier 4:** False Positives / Deprioritized
- **Visualization Suite:** Generates log-scale Period vs. Transit Depth population plots for paper publication.

## Repository Layout
- `src/query_tess.py`: Script for fetching TESS target metadata via APIs.
- `src/categorize_tiers.py`: Core logic for target classification into reliability tiers.
- `notebooks/generate_visualizations.ipynb`: Jupyter notebook for dataset summary statistics and plot export.
- `data/`: Directory containing output CSV logbooks.

## Installation & Setup
1. Clone this repository:
   ```bash
   git clone [https://github.com/wwwm-p/tess-triage-pipeline.git](https://github.com/wwwm-p/tess-triage-pipeline.git)
   cd tess-triage-pipeline
