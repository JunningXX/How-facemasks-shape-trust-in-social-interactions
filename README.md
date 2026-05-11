# How Facemasks Shape Trust in Social Interactions

[![DOI](https://img.shields.io/badge/DOI-10.1371/journal.pone.0331918-blue.svg)](https://doi.org/10.1371/journal.pone.0331918)
[![R](https://img.shields.io/badge/Language-R-276DC3.svg)](https://www.r-project.org/)

This repository contains the data and analysis code for the paper: **"How facemasks shape trust in social interactions"** published in *PLOS ONE*.

## 📖 Abstract

Face coverings can potentially impact how trustworthy someone appears through two channels: by hiding important facial cues associated with trust; or by signalling the wearer’s intentions or personal characteristics. The facemasks widely adopted during the COVID-19 pandemic both obscured the face and were associated with pro-social attitudes or intentions. 

The goal of this paper is to investigate how facemasks impact judgments about the trustworthiness of the wearer, and whether this would affect interactions with others. We report three experiments. Experiments 1 and 2 examined decisions in a two-player trust game when participants interacted with a single masked or unmasked counterpart. Experiment 3 explored whether participants were more likely to trust a masked or an unmasked person in a straight choice between them. 

In all experiments, masked faces were judged more trustworthy than unmasked ones. While in Experiments 1 and 2 this was not reflected in trust behaviour, in Experiment 3 over 70% of participants chose to trust the masked person, a decision predicted by the difference in perceived trustworthiness between the masked and unmasked counterparts. This suggests that in settings where facemasks or similar trust-related cues are more salient, such as in joint evaluation, they can lead to enhanced trust.

## 📈 Statistical Analysis & Methodology

To ensure robust and reliable conclusions, this project used a variety of statistical techniques to analyse both continuous and binary decision-making data. The analysis pipeline demonstrates proficiency in handling complex experimental designs, including repeated measures and counterbalanced conditions.

Key statistical methods employed in this project include:

* **Power Analysis:** Conducted post-hoc power analyses to verify that the sample sizes provided sufficient statistical power (e.g., > 0.9) to detect the primary effects across all experiments.
* **Linear Regression & Effect Sizes:** Performed linear regressions to evaluate the impact of experimental manipulations on continuous variables (e.g., trustor allocations and trustworthiness ratings), reporting comprehensive statistics including 95% confidence intervals and Cohen's *d* for effect sizes.
* **Multi-Level Modeling (Hierarchical Linear Models):** Implemented multi-level regressions to analyse data where participants provided multiple, non-independent responses (e.g., decisions made using the strategy method). These models successfully accounted for this lack of independence by incorporating both fixed effects (for experimental conditions, genders, and role order) and random effects for individual participants.
* **Logistic Regression & Contrast Coding:** Applied logistic regressions to model binary outcome variables, specifically when analysing straight-choice preference data. Contrast coding was used to re-centre categorical variables, allowing for the precise interpretation of intercepts as log-odds. 
* **Robustness Checks:** Validated the findings of the logistic regressions by running supplementary linear probability models to ensure the stability and reliability of the results. 
* **Mixed ANOVA:** Conducted 2x2 mixed ANOVAs to examine the main and interaction effects of within-subject and between-subject variables on perceptual ratings.

## 📂 Repository Structure

* `Experiment 1-3/` - Contains all materials for the three experiments, including:
  * Raw experimental data (`.csv` format)
  * R scripts for data cleaning, statistical analysis, and generating the paper's figures
  * Qualtrics surveys used for data collection
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

