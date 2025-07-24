# Analyzing Manchester United Goals: A Statistical Analysis of 2023/24 Premier League Passing Data

## Overview

This repository contains an R Markdown project analyzing Manchester United's performance in the 2023/24 Premier League season, focusing on passing and goal-scoring metrics. The analysis applies:

* **Count Models**: Log-linear, Poisson, Quasi-Poisson, and Negative Binomial models.
* **Non-Parametric Regression**: LOESS (Locally Estimated Scatterplot Smoothing).
* **Clustering Techniques**: Linear Mixed-Effects Models (LMM) and Hierarchical Clustering.

These methods are used to explore relationships between variables such as goals scored (**GF**), expected goals (**xG**), assists (**Ast**), and various passing statistics. The data is sourced from [FBref](https://fbref.com/en/).


## Repository Contents

* `manchester_united_analysis_202324.Rmd`: The main R Markdown file containing the complete analysis, including data loading, cleaning, exploratory data analysis (EDA), visualizations, correlation analysis, model fitting, and key insights.
* `MUFC_23_24_Passing_Data_Cleaned.xlsx`: The dataset (not included in the repository; **must be sourced separately**) containing match-level passing and performance metrics for Manchester United's 2023/24 season.
* `GLMs-in-MUFC-shot-analysis_files/`: Directory containing generated figures (e.g., plots for goals, correlations, LOESS regression) from rendering the R Markdown file.

## Prerequisites

To run the analysis, ensure you have the following installed:

* **R** (version 4.0 or higher)
* **RStudio** (recommended for rendering R Markdown)

### R Packages:

Install the following R packages:

* `dplyr` (data manipulation)
* `ggplot2` (visualizations)
* `MASS` (Negative Binomial model)
* `lme4` and `lmerTest` (Linear Mixed-Effects Models)
* `dendextend` (Hierarchical Clustering)
* `readxl` (reading Excel files)
* `corrplot` and `lares` (correlation analysis and visualization)

### Dataset:

Obtain the `MUFC_23_24_Passing_Data_Cleaned.xlsx` file from a reliable source (e.g., [FBref](https://fbref.com/en/squads/19538871/2023-2024/matchlogs/c9/passing/Manchester-United-Match-Logs-Premier-League)) or prepare a dataset with the required variables: `Date`, `Round`, `Day`, `Venue`, `Result`, `GF`, `GA`, `Opponent`, `Cmp`, `Att`, `Cmp%`, `TotDist`, `PrgDist`, `Ast`, `xAG`, `xA`, `KP`, `Final_3rd_passes`, `PPA`, `CrsPA`, `PrgP`, `xG`.

## Installation

1.  **Clone or download this repository:**
    ```bash
    git clone <your-repo-url>
    ```
2.  **Install the required R packages:**
    ```R
    install.packages(c("dplyr", "ggplot2", "MASS", "lme4", "lmerTest", "dendextend", "readxl", "corrplot", "lares"))
    ```
3.  **Place the `MUFC_23_24_Passing_Data_Cleaned.xlsx` file** in your R working directory or update the file path in the R Markdown code to match your local setup.

## Usage

1.  Open `manchester_united_analysis_202324.Rmd` in RStudio.
2.  Ensure the dataset path in the data loading section is correct. For example:
    ```R
    mufc_data <- read_excel("path/to/MUFC_23_24_Passing_Data_Cleaned.xlsx")
    ```
3.  **Render the R Markdown file** to generate the analysis report and visualizations:
    ```R
    library(rmarkdown)
    render("manchester_united_analysis_202324.Rmd")
    ```
    The output will include an HTML or Markdown report with all analyses, plots, and insights, saved in the working directory along with a figures folder (`GLMs-in-MUFC-shot-analysis_files/`).

## Project Structure

The `manchester_united_analysis_202324.Rmd` file is organized as follows:

* **Introduction**: Overview of the analysis objectives and data source.
* **Data Loading and Preparation**: Loads and cleans the dataset, converting variables to appropriate formats.
* **Exploratory Data Analysis (EDA)**: Summarizes match results, goals, passing stats, and advanced metrics (e.g., xG, xA).
* **Visualizations**: Includes plots for goals for/against by round, venue, opponent, and key passes, plus result distributions.
* **Correlation Analysis**: Examines relationships between variables (e.g., GF, xG, Ast) using correlation matrices and plots.
* **Model Fitting**: Applies Log-linear, Poisson, Quasi-Poisson, and Negative Binomial models to predict goals scored (**GF**).
* **Non-Parametric Regression**: Uses LOESS to model the non-linear relationship between **xG** and **GF**.
* **Clustered Observations**: Fits a Linear Mixed-Effects Model with opponent as a random effect and performs hierarchical clustering.
* **Key Takeaways**: Summarizes critical findings, highlighting the importance of assists, xG, and tactical implications.

## Key Findings

* **Assists Drive Goals**: Assists (**Ast**) are strongly associated with goals scored (**GF**, p < 0.001), emphasizing the role of playmaking.
* **xG Predicts Scoring**: Expected goals (**xG**) significantly predict **GF** (p = 0.002 in LMM), but a LOESS model shows a plateau at high **xG** values, suggesting finishing inefficiencies.
* **Limited Impact of Other Metrics**: Metrics like **xA**, **xAG**, **KP**, and **CrsPA** show weak associations with **GF**, indicating less direct influence on scoring.
* **Passing Dynamics**: High correlations between passing metrics (**Cmp**, **Att**, **TotDist**) suggest a possession-based style, but these do not strongly correlate with goals.
* **Opponent Effects Minimal**: The LMM indicates negligible opponent-specific variability in **GF**, suggesting consistent performance across matches.
* **Tactical Insights**: Variability in mid-range **xG** (1.5–2) and a plateau at higher **xG** highlight areas for improving finishing and playmaker coordination.

## Notes

* The Negative Binomial model may produce warnings about iteration limits due to a high theta value, but this does not affect the results significantly, as the data closely follows a Poisson distribution.
* Ensure the dataset matches the expected structure (22 variables as listed). If using a different dataset, adjust column names in the R Markdown code accordingly.
* The analysis assumes no missing data; verify the dataset for completeness before running.

## Author

Wayne Chilionje

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

* Data sourced from [FBref](https://fbref.com/en/).
* Built with R, RStudio, and various R packages for statistical analysis and visualization.
