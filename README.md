Automated TESS Exoplanet Triage & Architectural Prioritization Pipeline

An end-to-end Python software pipeline for fetching, cross-referencing, and categorizing NASA TESS (Transiting Exoplanet Survey Satellite) Objects of Interest (TOIs) into operational reliability tiers.

Overview

Space telescopes like TESS generate thousands of Threshold Crossing Events (TCEs). Distinguishing genuine planetary transits from background eclipsing binaries and instrumental artifacts is computationally intensive.

This repository provides an automated data pipeline that:

Programmatically queries the ExoFOP and ExoMAST public APIs.

Evaluates system multiplicity (boosting candidates in multi-planet architectures).

Assigns candidates into actionable reliability tiers (Tier 1 through Tier 4).

Outputs publication-ready summary statistics and logbooks for astronomical follow-up.

Reliability Tier Framework

Tier

Description

Action / Recommendation

Tier 1

Confirmed Planets (CP)

Literature Benchmark

Tier 2

High-Priority Multi-Planet Candidates

Priority Queue for Statistical Validation

Tier 3

Single Planet Candidates

Manual DV & Centroid Inspection Required

Tier 4

Known False Positives (FP)

Automated Rejection / Deprioritized

Project Structure

├── main_triage_pipeline.py    # Primary API query & data triage script
├── generate_plots.py          # Visualization script for Period vs. Depth plots
├── requirements.txt           # Python package dependencies
├── tess_exoplanet_validation_logbook.csv  # Output data logbook
└── README.md                  # Project documentation


Installation & Usage

1. Clone the Repository

git clone https://github.com/wwwm-p/tess-triage-pipeline.git
cd tess-exoplanet-triage-pipeline


2. Install Dependencies

pip install -r requirements.txt


3. Run the Pipeline

python main_triage_pipeline.py


4. Generate Visualizations

python generate_plots.py


Citation & References

Ricker, G. R., et al. (2015). Transiting Exoplanet Survey Satellite (TESS). JATIS, 1(1), 014003.

Guerrero, N. M., et al. (2021). The TESS Objects of Interest Catalog from the Prime Mission. ApJS, 254(2), 39.

Lissauer, J. J., et al. (2012). Almost All of Kepler's Multiple-Planet Candidates Are Valid Planets. ApJ, 750(2), 112.
