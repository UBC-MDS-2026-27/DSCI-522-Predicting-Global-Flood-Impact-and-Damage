# DSCI-522-Predicting-Global-Flood-Impact-and-Damage

## Authors:
- Niroshan Benjamin
- Fang Fang
- Abdullah Naeem
- Everett Rendon

## Project Summary:
Could we predict whether a flood causes at least one death based on its location,duration and other affection to human? Our team compared several classification model and choosed a tuned decision tree model which perform best. It achieved an F1 score of 0.6633 and identified about 70% of fatal events on test data set. This project suggested that we have reason to believe the recorded event characteristics contain useful information about fatality. 

## How to run the analysis:
Clone the repository and enter the project directory:

```bash
git clone https://github.com/UBC-MDS-2026-27/DSCI-522-Predicting-Global-Flood-Impact-and-Damage.git
cd DSCI-522-Predicting-Global-Flood-Impact-and-Damage
```

Install the Python environment with uv:
```bash
uv sync
```

With Quarto installed, render the report from the project directory:
```bash
uv run quarto render analysis/flood_fatality_prediction_report.qmd
```

Open `analysis/flood_fatality_prediction_report.html` to read the rendered report. 
The required Excel data file is included at `data/raw/Aggregated_Flood_Data.xlsx`.

## Dependencies:
- Python (required version in [pyproject.toml](pyproject.toml))
- uv for installing the python environment(version 0.12 or higher)
- quarto for rendering report(version 1.10 or higher)
Python packages needed are listed in [pyproject.toml](pyproject.toml). The environment is locked in [uv.lock](uv.lock).

## Licenses:
The software code contained within this repository is licensed under the MIT license. The report is licensed under the CC BY-NC-ND 4.0. See [LICENSE.md](LICENSE.md) for the licenses covering the project code and report. 

## AI use statement:

## Link to the rendered report:
[View the report](analysis/flood_fatality_prediction_report.html)
