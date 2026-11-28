# DSCI-522-Predicting-Global-Flood-Impact-and-Damage

## Authors:

- Niroshan Benjamin
- Fang Fang
- Abdullah Naeem
- Everett Rendon

## Project Summary:

Could we predict whether a flood causes at least one death based on its location and other characteristics related to impact? Our team compared several classification models and chose a tuned decision tree model that performed best and generalized well on the test data set. It achieved a test F1 score of 0.6114 and a test accuracy of 84.13%. From this model, we were able to identify about 73% of fatal events on the test data set. This project suggested that we have reason to believe the recorded event characteristics contain useful information about fatality.

## How to run the analysis:
Clone the repository and enter the project directory:
``` bash
git clone https://github.com/UBC-MDS-2026-27/DSCI-522-Predicting-Global-Flood-Impact-and-Damage.git
cd DSCI-522-Predicting-Global-Flood-Impact-and-Damage
```
Create an SSH key if you do not already have one (press Enter at each prompt; without it, Docker creates a folder at `~/.ssh/id_ed25519.pub` and SSH into the container fails until you delete that folder and create the key):
``` bash
ssh-keygen -t ed25519
```
With Docker Desktop running, download the project image:
``` bash
docker compose pull
```
Render the report inside the container:
``` bash
docker compose run --rm analysis-env uv run quarto render analysis/flood_fatality_prediction_report.qmd
```
Because `--rm` is used, the container stops and removes itself automatically when rendering finishes (if you start it with `docker compose up -d`, stop and remove it with `docker compose down`).

Open `analysis/flood_fatality_prediction_report.html` to read the rendered report. Or run the following command from the project root directory:

- macOS:
```bash
open analysis/flood_fatality_prediction_report.html
```

- Windows (PowerShell):
```powershell
start analysis/flood_fatality_prediction_report.html
```

The required Excel data file is included at `data/raw/Aggregated_Flood_Data.xlsx`.


For instructions on editing the code, adding packages, or contributing to this project, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Dependencies:
- Docker Desktop (the container defined by [Dockerfile](Dockerfile) and [docker-compose.yml](docker-compose.yml) includes Python, `uv`, Quarto, and all required packages)
- Git

Python packages needed are listed in [pyproject.toml](pyproject.toml). The environment is locked in [uv.lock](uv.lock).

## Licenses:

The software code contained within this repository is licensed under the MIT license. The report is licensed under the CC BY-NC-ND 4.0. See [LICENSE.md](LICENSE.md) for the licenses covering the project code and report.

## AI use statement:
Fang Fang: I used Chatgpt to teach me how I can insert a link to other file in the repository.
Example prompts: "how I can insert a link to other file in the repository?"


Everett Rendon: The LLM I utilized to assist with my portion of the report was ChatGPT. I utilized it to generate some of the trivial plotting code in the Discussion section of the report and for some instructions on managing uv, such as a bugfix with pyproject.toml in which a folder was being generated under the assumption our project was to contain exportable functions, which it did not. It also acted as a spellcheck and proofreader after I had completed the methods, analysis, and discussion sections where it caught some small typos and old information that needed updating as our report structure changed.

Example prompts: `What code can be utilized to display the confusion matrix cleanly?` `Given this traceback, how do I resolve this uv error?` `How can I display the count of rows containing NA's?`

Niroshan Benjamin: I used Google Antigravity (Gemini and Claude models) to refine the investigative question, draft and review my preprocessing, cross-validation, and hyperparameter tuning code in modelling.ipynb, check for data leakage, draft concise GitHub issue and pull request descriptions, and troubleshoot Git/GitHub workflow steps. No custom instruction or system prompt files were used.

Example prompts:

- Check my modelling file to see if the train/test split, preprocessing pipeline, and cross-validation are correct and follow the milestone requirements

- What do I need to change in my notebook to switch from the DesInventar sheet to the Aggregated sheet?

Abdullah Naeem: In this project, I used Kiro and Google Antigravity (Claude and Gemini) to proofread and refine my portion of the exploratory data analysis and visualizations. I used them to get ideas on what visualizations might help with understanding the data based on the EDA process. I also used them to help with proofreading my writing for my section of the report. No custom instructions or system files were used from my end.

Example Prompts:

- "Check over my data visualizations and EDA to see if the chosen visualizations are relevant to the investigative question and that they follow the milestone criteria."

- "Can you proofread my writing for my section of the report and check for typos, grammatical errors, and clarity?"

## Link to the rendered report:

[View the rendered report on GitHub Pages](https://ubc-mds-2026-27.github.io/DSCI-522-Predicting-Global-Flood-Impact-and-Damage/)