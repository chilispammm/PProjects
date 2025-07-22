# Football Analytics Portfolio

Welcome to my collection of football analytics projects. This repository showcases my work in football data analysis, focusing on Premier League performance metrics, statistical modeling, and data visualization.

## Featured Projects

### 1. Manchester United 2023/24 Season Analysis
📊 **GLM Analysis of MUFC Goals with Passing Data**  
[View Analysis](./GLMs%20to%20analyze%20MUFC%20Goals%20with%20Passing%20data/GLMs-in-MUFC-shot-analysis.md)
- Applied Generalized Linear Models (Poisson, Quasi-Poisson, Negative Binomial) to analyze goal-scoring patterns
- Investigated relationships between passing metrics, xG, and actual goals scored
- Visualized key performance indicators and match outcomes
- Identified strengths and areas for improvement in Manchester United's attacking play

### 2. Premier League Forward Performance Analysis
[View Analysis](./Multinomial%20and%20Generalized%20Linear%20Model%20Applications%20in%20Analyzing%20Premier%20League%20Forward%20Performance/Regression-techniques-in-football.md)
- Multinomial and generalized linear models for forward performance evaluation
- Analysis of goal scoring patterns and shot conversion rates
- Expected Goals (xG) and non-penalty goal analysis
- Performance comparison across different playing positions

## Technical Approach

### Statistical Modeling
- **Generalized Linear Models (GLMs)**: For count data analysis of goals and assists
- **Multinomial Regression**: For categorical outcome prediction
- **Mixed-Effects Models**: Accounting for team and opponent variability
- **Time Series Analysis**: Tracking performance trends across the season

### Data Visualization
- Interactive plots for performance metrics
- Heatmaps of shot locations and passing networks
- Comparative analysis of actual vs. expected performance

## Data Sources
- [FBref](https://fbref.com/): Premier League match and player statistics
- [Understat](https://understat.com/): Advanced metrics including xG and xA
- [WhoScored](https://www.whoscored.com/): Player ratings and match statistics

## Getting Started

### Prerequisites
- R (≥ 4.0.0)
- RStudio (recommended)
- Required R packages: tidyverse, lme4, MASS, ggplot2, performance

### Installation

1. Clone the repository:
```bash
git clone https://github.com/chilispammm/PProjects.git
```

2. Open the R Markdown (`.Rmd`) file in RStudio
3. Install required packages:
```r
install.packages(c("tidyverse", "lme4", "MASS", "ggplot2", "performance"))
```
4. Click "Knit" to reproduce the analysis

## Project Status
- ✅ Manchester United 2023/24 Analysis - Complete
- ✅ Premier League Forward Performance - Complete
- 📊 Additional team analyses - Planned

## Key Findings
- Strong correlation between key passes and goal-scoring outcomes
- Significant impact of xG on match results
- Identified patterns in team performance against different opposition styles

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
