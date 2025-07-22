# Premier League Forward Performance Analysis

This project analyzes Premier League forward performance using statistical modeling techniques, specifically multinomial and generalized linear models. The analysis focuses on the 2023-2024 Premier League season.

## Project Overview

The project explores various aspects of forward performance in the Premier League, including:
- Goal scoring patterns
- Shot conversion rates
- Expected Goals (xG) analysis
- Penalty kick performance
- Non-penalty goal analysis

## Data

The analysis is based on Premier League shooting data from the 2023-2024 season, contained in:
- `files/23_24 PL Shooting Data.xlsx`

## Key Files

- `Regression techniques in football.Rmd`: Main analysis file containing the R code and markdown documentation
- `Regression-techniques-in-football.md`: Rendered version of the analysis
- `Regression-techniques-in-football_files/`: Directory containing generated plots and figures
- `netlify.toml`: Configuration for web deployment

## Requirements

To run this analysis, you will need:
- R and RStudio
- Required R packages (installed automatically when running the Rmd file)

## Running the Analysis

1. Clone this repository
2. Open `Regression techniques in football.Rmd` in RStudio
3. Click "Knit" to generate the analysis report

## Project Structure

```
.
├── Regression techniques in football.Rmd      # Main analysis file
├── Regression-techniques-in-football.md       # Rendered analysis
├── Regression-techniques-in-football_files/   # Generated plots
├── files/                                    # Data directory
│   └── 23_24 PL Shooting Data.xlsx          # Premier League data
│   └── images/                              # Additional images
├── netlify.toml                             # Web deployment config
└── .gitignore                              # Git ignore rules
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

Wayne Chilionje

## Acknowledgments

- Data source: Fbref
- Analysis methodology inspired by modern football analytics approaches
