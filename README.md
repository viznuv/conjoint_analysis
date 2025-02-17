# Conjoint Analysis for Service Preferences

This project applies **Conjoint Analysis** using **Ordinary Least Squares (OLS) Regression** to evaluate meal component preferences based on **average ratings** from a dataset of BBQ meal bundles. The model estimates the part-worth utilities of different meal components and predicts the best and worst combinations.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)


---

## Overview

**Conjoint Analysis** is a statistical technique used in marketing to determine how different features of a product influence consumer preferences. In this project, we:

- **Analyze meal preferences** based on different components (e.g., starter, main dishes, side, dessert).
- **Use a regression-based approach** to estimate part-worth utilities (preference scores).
- **Predict the best and worst meal combinations** based on estimated ratings.

This approach helps in **menu optimization, pricing strategies, and marketing research**.

---

## Features

- **Data Import & Processing:** Reads meal component data from a CSV file.
- **OLS Regression Model:** Estimates the impact of each meal component on average ratings.
- **Prediction of Meal Ratings:** Uses the trained model to predict ratings for all possible meal combinations.
- **Identification of Best & Worst Combinations:** Finds the most and least preferred meal combinations.

---

## Prerequisites

- Python 3.x
- [Pandas](https://pandas.pydata.org/)
- [Statsmodels](https://www.statsmodels.org/stable/index.html)

---

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/viznuv/conjoint-analysis.git
   cd conjoint-analysis


Code Description

1. Data Import & Preprocessing
Reads bbq_summer.csv, which contains meal components and their respective average ratings.
Converts categorical columns (starter, maindishI, maindishII, side, dessert) into categorical variables.

2. OLS Regression Model
Fits a linear regression model with the formula:
avg_rating ~ C(starter) + C(maindishI) + C(maindishII) + C(side) + C(dessert)

This allows us to estimate the part-worth utilities (preference scores) for each meal component.

3. Generating All Possible Meal Combinations
Extracts all unique levels of each meal component.
Uses itertools.product() to generate every possible meal bundle.

4. Predicting Ratings for Meal Combinations
Uses the trained model to predict the average rating for each combination.

5. Identifying Best & Worst Meal Combinations
The highest-rated meal combination is identified as best.
The lowest-rated meal combination is identified as worst.
