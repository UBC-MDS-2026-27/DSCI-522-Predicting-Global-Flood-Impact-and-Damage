# DSCI-522-Predicting-Global-Flood-Impact-and-Damage

## Authors:

- Niroshan Benjamin
- Fang Fang
- Abdullah Naeem
- Everett Rendon

## Project Summary:

Could we predict whether a flood causes at least one death based on its location and other affection to human? Our team compared several classification model and choosed a tuned decision tree model which perform best. It achieved an F1 score of 0.6633 and identified about 70% of fatal events on test data set. This project suggested that we have reason to believe the recorded event characteristics contain useful information about fatality.

## How to run the analysis:

Clone the repository and enter the project directory:

``` bash
git clone https://github.com/UBC-MDS-2026-27/DSCI-522-Predicting-Global-Flood-Impact-and-Damage.git
cd DSCI-522-Predicting-Global-Flood-Impact-and-Damage
```

Install the Python environment with uv:

``` bash
uv sync
```

With Quarto installed, render the report from the project directory:

``` bash
uv run quarto render analysis/flood_fatality_prediction_report.qmd
```

Open `analysis/flood_fatality_prediction_report.html` to read the rendered report. The required Excel data file is included at `data/raw/Aggregated_Flood_Data.xlsx`.

## Dependencies:

- Python (required version in [pyproject.toml](pyproject.toml))
- uv for installing the python environment(version 0.12 or higher)
- quarto for rendering report(version 1.10 or higher) Python packages needed are listed in [pyproject.toml](pyproject.toml). The environment is locked in [uv.lock](uv.lock).

## Licenses:

The software code contained within this repository is licensed under the MIT license. The report is licensed under the CC BY-NC-ND 4.0. See [LICENSE.md](LICENSE.md) for the licenses covering the project code and report.

## AI use statement:

Everett Rendon: The LLM I utilized to assist with my portion of the report was ChatGPT. I utilized it to generate some of the trivial plotting code in the Discussion section of the report and for some instructions on managing uv, such as a bugfix with pyproject.toml in which a folder was being generated under the assumption our project was to contain exportable functions, which it did not. It also acted as a spellcheck and proofreader after I had completed the methods, analysis, and discussion sections where it caught some small typos and old information that needed updating as our report structure changed.

Niroshan Benjamin: I used Google Antigravity (Gemini and Claude models) to refine the investigative question, draft and review my preprocessing, cross-validation, and hyperparameter tuning code in modelling.ipynb, check for data leakage, draft concise GitHub issue and pull request descriptions, and troubleshoot Git/GitHub workflow steps. No custom instruction or system prompt files were used.

Example prompts:

-Check my modelling file to see if the train/test split, preprocessing pipeline, and cross-validation are correct and follow the milestone requirements

-What do I need to change in my notebook to switch from the DesInventar sheet to the Aggregated sheet?

Abdullah Naeem: In this project, I used Kiro and Google Antigravity (Claude and Gemini) to proofread and refine my portion of the exploratory data analysis and visualizations. I used them to get ideas on what visualizations might help with understanding the data based on the EDA process. I also used them to help with proofreading my writing for my section of the report. No custom instructions or system files were used from my end.

Example Prompts:

- "Check over my data visualizations and EDA to see if the chosen visualizations are relevant to the investigative question and that they follow the milestone criteria."

- "Can you proofread my writing for my section of the report and check for typos, grammatical errors, and clarity?"

## Link to the rendered report:

[View the report](analysis/flood_fatality_prediction_report.html)