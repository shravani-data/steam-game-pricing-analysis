# SteamScope Pricing Analysis
#### Auditing and Rebuilding a Flawed Data Pipeline

## Overview

This project simulates a real-world data consultancy scenario at SteamScope Analytics, a fictional gaming analytics firm that advises indie game studios on pricing strategy. The objective was to audit an inherited data pipeline for hidden quality issues, diagnose how those issues broke statistical assumptions, and rebuild the pipeline and pricing model using best practices.

The project involved reverse-engineering an existing analytics workflow, auditing it against data integrity principles, running formal regression diagnostics, and rebuilding the pipeline and model end-to-end.
**Full Report:** [View PDF Report](steam_game_pricing_analysis.pdf)

## Business Scenario

SteamScope Analytics produces a quarterly market report answering one question for its clients: *"How much are consumers willing to pay for games like yours?"* The previous Senior Analyst, Avery, was let go after it was discovered that their pricing reports contained systematic errors, leading to badly flawed recommendations for major clients.

Before the pipeline could be replaced, it first had to be reverse-engineered and reproduced exactly (since downstream client dashboards depended on Avery's exact output format), then audited to identify the specific mistakes, and finally rebuilt into a statistically sound Version 2.0.

The analysis focused on answering key questions:

- What data quality issues were hidden inside Avery's original pipeline, and how did they distort the pricing model?
- Which of Avery's data wrangling decisions were legitimate, and which were genuine errors?
- Does a corrected pipeline produce a more reliable and interpretable pricing model?
- Which factors (genre, popularity, review sentiment, platform availability) actually drive game pricing?

## Analytical Workflow

#### 1. Legacy Pipeline Reconstruction
- Reverse-engineered the original cleaning pipeline using reproducible tidyverse workflows.
- Verified the reconstructed dataset matched the legacy output exactly.

#### 2. Data Quality Audit
Identified issues including:
- Incorrect unit conversion
- Arbitrary price capping
- Missing data handling bias
- Incorrect categorical variable encoding

#### 3. Model Diagnostics
- Applied residual diagnostics to evaluate regression assumptions.
- Identified how data manipulation affected model reliability.

#### 4. Pipeline Rebuild & Modelling
- Developed a corrected Version 2.0 pipeline.
- Improved feature handling and refitted the pricing model.

#### 5. Business Insights
- Improved model explanatory power from R² = 0.049 to R² = 0.310.
- Identified significant pricing drivers including genre, review sentiment, player popularity, and platform availability.
  
## Tools & Technologies

**Programming & Analysis**
- R
- Tidyverse
- lubridate
- ggplot2

**Statistical Methods**
- Multiple linear regression
- Residual diagnostics (`ggResidpanel`)
- Exploratory pairwise analysis (`GGally::ggpairs`)
- Data quality and missing-data auditing

**Reporting**
- Quarto

## Skills Demonstrated

- Data quality auditing
- Reproducible data pipeline construction
- Regression modelling & diagnostics
- Statistical reasoning
- Data visualisation
- Business-focused reporting and stakeholder communication

## Project Context

This project was developed as part of postgraduate Business Analytics coursework at Monash University and structured as a professional analytics case study.
