# How Facemasks Shape Trust in Social Interactions

[![DOI](https://img.shields.io/badge/DOI-10.1371/journal.pone.0331918-blue.svg)](https://doi.org/10.1371/journal.pone.0331918)
[![R](https://img.shields.io/badge/Language-R-276DC3.svg)](https://www.r-project.org/)

This repository contains the data and analysis code for the paper: **"How facemasks shape trust in social interactions"** published in *PLOS ONE*.

## 📖 Abstract

Face coverings can potentially impact how trustworthy someone appears through two channels: by hiding important facial cues associated with trust; or by signalling the wearer’s intentions or personal characteristics. The facemasks widely adopted during the COVID-19 pandemic both obscured the face and were associated with pro-social attitudes or intentions. 

The goal of this paper is to investigate how facemasks impact judgments about the trustworthiness of the wearer, and whether this would affect interactions with others. We report three experiments. Experiments 1 and 2 examined decisions in a two-player trust game when participants interacted with a single masked or unmasked counterpart. Experiment 3 explored whether participants were more likely to trust a masked or an unmasked person in a straight choice between them. 

In all experiments, masked faces were judged more trustworthy than unmasked ones. While in Experiments 1 and 2 this was not reflected in trust behaviour, in Experiment 3 over 70% of participants chose to trust the masked person, a decision predicted by the difference in perceived trustworthiness between the masked and unmasked counterparts. This suggests that in settings where facemasks or similar trust-related cues are more salient, such as in joint evaluation, they can lead to enhanced trust.

## 📂 Repository Structure

* `data/` - Contains the raw experimental data in `.csv` format (includes `Experiment_1.csv`).
* `scripts/` - Contains the R scripts used for data cleaning, statistical analysis, and generating the figures presented in the paper.
* `README.md` - Project documentation.

## 📊 Data Description

All data necessary to reproduce the findings are included in this repository. 

For example, `Experiment_1.csv` contains 804 observations and 38 variables. Key variables across the datasets include:
* **Demographics:** Age, sex, ethnicity, highest education level, and nationality.
* **Experimental Conditions:** Stimulus shown (`Pic.Mask`: Masked/Unmasked, `Pic.Gender`).
* **Game/Behavioral Measures:** Responses for both Senders and Responders in the Trust Game (e.g., `Sender_Response`, `Responder_3` to `Responder_30`).
* **Perceptual Judgements:** Ratings of counterpart `Trustworthy` and `Attractiveness`.
* **Attitudes:** Variables mapping COVID-19 vaccine attitudes (`COVID_19_vaccine`), mask attitudes (`Mask_attitude`), and beliefs about mask efficacy.
* **Comprehension:** Checks for experiment instruction understanding (`Instruction_1` to `Instruction_4`, `understanding_difficulty`).

## 💻 Tech Stack & Dependencies

The analysis for this project was conducted in **R**. To run the scripts, you will need the following R packages installed:

* `tidyverse` (for data manipulation and pipeline)
* `ggplot2` (for data visualization)
* `lme4` (for fitting linear mixed-effects models)

You can install the required packages in R using the following command:
```R
install.packages(c("tidyverse", "ggplot2", "lme4"))
