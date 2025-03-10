# Human Freedom Index Analysis

This repository contains an exploratory analysis of the Human Freedom Index (HFI) dataset from 2008-2016. The analysis investigates relationships between different components of freedom, including personal, economic, and rule of law metrics.

## Overview

The Human Freedom Index is an annual report co-published by the Cato Institute, the Fraser Institute, and the Liberales Institut at the Friedrich Naumann Foundation for Freedom. It attempts to measure "freedom" through various variables across countries worldwide, serving as an objective measure for understanding the relationships between different types of freedom and social and economic circumstances.

## Dataset

The dataset (`hfi`) contains:
- 1,458 observations (country-year combinations)
- 123 variables measuring various aspects of freedom
- Data covering years 2008-2016
- Regional information for countries
- Detailed scores for personal freedom (pf) and economic freedom (ef) components

## Analysis Highlights

### Key Relationships Investigated:

1. **Freedom of Expression & Personal Freedom**
   - Strong positive correlation (r = 0.796)
   - ~63% of variation in personal freedom scores explained by expression control
   - Linear relationship confirmed through residual analysis

2. **Rule of Law & Economic Freedom**
   - Strong positive correlation (r = 0.71)
   - ~50% of variation in economic freedom explained by rule of law
   - Confirms theoretical relationship between legal systems and economic activity

3. **Criminal Justice & Personal Freedom**
   - Strong positive correlation (r = 0.68)
   - ~47% of variation in personal freedom explained by criminal justice quality
   - Important but not as predictive as expression rights

4. **Religious Freedom & Economic Freedom**
   - Surprisingly weak correlation (r = 0.13)
   - <2% of variation in economic freedom explained by religious freedom
   - Suggests independence between cultural and economic freedoms

### Methodology:
- Linear regression models to quantify relationships
- Visual analysis through scatterplots with regression lines
- Model diagnostics including residual analysis, Q-Q plots, and distribution checks
- Correlation analysis to measure relationship strength

## Key Findings

1. Freedom is multidimensional, with different components showing varying degrees of correlation
2. Freedom of expression is the strongest predictor of overall personal freedom
3. Rule of law provides a foundation for both personal and economic freedoms
4. Some freedoms (like religious and economic) can develop independently
5. Linear models appropriately capture most relationships between freedom components

## Requirements

This analysis was performed using R with the following packages:
- tidyverse (for data manipulation and visualization)
- openintro (contains the hfi dataset)

```r
# Load required packages
library(tidyverse)
library(openintro)

# Load the dataset
data('hfi', package='openintro')
```

## Files in this Repository

- `freedom_analysis.Rmd`: R Markdown file containing the complete analysis
- `freedom_analysis.html`: Rendered analysis with visualizations and interpretations
- `plots/`: Directory containing generated visualizations
- `data/`: Directory containing processed datasets

## Visualizations

The repository includes several key visualizations:
- Scatterplots showing relationships between various freedom metrics
- Residual plots for model diagnostics
- Q-Q plots for normality assessment
- Histograms of residual distributions

## Potential Applications

This analysis can inform:
- Policy development for promoting different aspects of freedom
- Understanding how freedoms interact in different cultural contexts
- Identifying which institutional foundations are most critical for specific freedoms
- Recognizing that enhancing one type of freedom doesn't automatically improve all others

## Future Work

Potential extensions of this analysis include:
- Longitudinal analysis to track freedom changes over time
- Cluster analysis to identify country groupings with similar freedom profiles
- Causal analysis to understand directional relationships between freedoms
- Incorporating additional years of data as they become available

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- The Cato Institute, Fraser Institute, and Liberales Institut for creating and maintaining the Human Freedom Index
- OpenIntro for making the dataset accessible for analysis
