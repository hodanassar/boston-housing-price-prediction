# Boston Housing Price Prediction

![R](https://img.shields.io/badge/R-Programming-blue)
![R Markdown](https://img.shields.io/badge/R-Markdown-blue)
![Regression](https://img.shields.io/badge/Regression-Modeling-green)
![Random Forest](https://img.shields.io/badge/Random%20Forest-Best%20Model-orange)
![Data Mining](https://img.shields.io/badge/Data-Mining-purple)

This project compares multiple supervised learning models to predict median home values using the Boston Housing dataset. The goal is to evaluate which modeling approach provides the strongest out-of-sample predictive performance and identify the most important drivers of housing value.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Models Used](#models-used)
- [Key Results](#key-results)
- [Model Performance Summary](#model-performance-summary)
- [Tools and Technologies](#tools-and-technologies)
- [Project Files](#project-files)
- [Author](#author)

## Project Overview

The Boston Housing dataset is a classic regression dataset used to study the relationship between housing values and neighborhood, structural, and environmental factors.

In this project, several supervised learning models were developed and compared to predict `medv`, the median value of owner-occupied homes. The models were evaluated using both in-sample and out-of-sample performance metrics, with the final recommendation based on out-of-sample MSPE.

## Dataset

The project uses the Boston Housing dataset, originally from Harrison and Rubinfeld (1978) and available through the `MASS` package in R.

The dataset includes:

- 506 observations
- 13 predictor variables
- Response variable: `medv`, median value of owner-occupied homes in $1000s

Key predictors include:

- `rm` — average number of rooms per dwelling
- `lstat` — percentage of lower-status population
- `crim` — per capita crime rate
- `nox` — nitric oxides concentration
- `tax` — property tax rate
- `ptratio` — pupil-teacher ratio

## Methodology

The project followed a supervised learning workflow:

1. Loaded and explored the Boston Housing dataset
2. Split the data into training and testing sets
3. Trained multiple regression models
4. Evaluated in-sample performance using ASE
5. Evaluated out-of-sample performance using MSPE
6. Compared model performance across methods
7. Identified the strongest predictors using feature importance
8. Selected the best-performing model based on test performance

## Models Used

The following supervised learning models were developed and compared:

- Linear Regression
- Pruned Regression Tree
- K-Nearest Neighbors
- Random Forest
- Boosting
- Generalized Additive Model
- Neural Network

## Key Results

Random Forest achieved the strongest out-of-sample performance, with the lowest MSPE of 11.80.

The analysis showed that:

- Random Forest was the best-performing model overall
- Ensemble and nonlinear models performed better than simpler linear models
- `rm` and `lstat` were the most important predictors
- Higher average number of rooms was associated with higher median home value
- Higher percentage of lower-status population was associated with lower median home value

## Model Performance Summary

| Rank | Model | Description | ASE | MSPE |
|---:|---|---|---:|---:|
| 1 | Random Forest | Ensemble of trees using bootstrap samples and random predictor subsets | 2.14 | 11.80 |
| 2 | Boosting | Sequential trees that improve prediction by learning from previous errors | 2.25 | 12.48 |
| 2 | Neural Network | Hidden-layer model using scaled variables to capture nonlinear patterns | 4.77 | 12.48 |
| 3 | GAM | Flexible model using smooth functions for nonlinear relationships | 8.16 | 14.79 |
| 4 | Pruned Regression Tree | Tree model pruned using cross-validated complexity parameter | 9.73 | 18.92 |
| 5 | K-NN | Distance-based model using scaled predictors | 6.18 | 20.57 |
| 6 | Linear Regression | Stepwise variable selection for linear prediction | 20.64 | 28.22 |

## Tools and Technologies

- R
- R Markdown
- MASS
- Random Forest
- Boosting
- GAM
- Neural Networks
- Regression Modeling
- Data Visualization

## Project Files

- `analysis/` — R Markdown analysis file containing data preparation, model training, evaluation, and comparison
- `presentation/` — cleaned presentation slides summarizing the methodology, results, and recommendations

## Author

Hoda Nassar
