<h1 align="center">A/B Testing Analysis: Landing Page Conversion Rates</h1>

## Overview

This repository contains an analysis of an A/B test comparing conversion rates between two landing pages: an existing page (control, `old_page`) and a new design (treatment, `new_page`). The goal is to determine if the new landing page improves user conversion rates.

## Project Idea

The project aims to evaluate the effectiveness of a redesigned landing page in improving user conversion rates, a critical metric for online businesses. The idea stems from the hypothesis that a modernized design could enhance user engagement and increase the likelihood of conversions (e.g., purchases or sign-ups). By conducting an A/B test, the analysis seeks to provide data-driven insights to decide whether to implement the new design or retain the existing one, optimizing the website's performance and user experience.

## Files

- `AB_Test_LandingPage_Conversion.ipynb`: Jupyter notebook with the full analysis, including data loading, cleaning, exploratory data analysis, hypothesis testing, and conclusions.
- `AB_Test_Summary.pdf`: PDF summary of the key findings and recommendations generated from the analysis.
- `README.md`: This file, providing an overview of the project.

## Data

- **Source**: The dataset (`ab_data.csv`) contains user interactions with columns: `user_id`, `timestamp`, `group`, `landing_page`, and `converted` (1 for conversion, 0 otherwise).
- **Sample Size**: 294,478 total entries, with 145,274 in the control group and 145,311 in the treatment group after cleaning.

## Analysis Summary

- **Conversion Rates**: Control group: 12.04%, Treatment group: 11.88%.
- **Difference**: -0.16% (Treatment slightly lower than Control).
- **95% Confidence Interval**: \[-0.39%, 0.08%\] (includes zero, indicating no significant difference).
- **P-value**: 0.1899 (not significant at (\\alpha = 0.05)).
- **Conclusion**: The new landing page does not significantly improve conversion rates.

## Methodology

1. **Data Cleaning**: Removed mismatches between `group` and `landing_page` (3,893 rows) and one duplicate `user_id`.
2. **Exploratory Analysis**: Visualized conversion counts by group.
3. **Hypothesis Testing**: Conducted a two-sample proportions z-test.
4. **Confidence Interval**: Calculated a 95% CI for the difference in conversion rates.

## Recommendations

- Retain the current (`old_page`) landing page.
- Consider extending the test duration for more data.
- Explore alternative designs or features for the landing page.
- Analyze user subgroups for potential segment-specific effects.

## Usage

- Open `AB_Test_LandingPage_Conversion.ipynb` in Jupyter Notebook or a compatible environment to review the full analysis.
- View `AB_Test_Summary.pdf` for a concise report of the findings.

## Repository

- https://github.com/AAMMMRRR/A-B-Testing-Analysis
