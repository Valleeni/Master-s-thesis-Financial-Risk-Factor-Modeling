# Master's Thesis: Financial Risk-Factor Modeling: A Comparison of Characteristic and Statistical Risk-Factor Models for Forecasting Portfolio Risk in Norway

This repository contains all code used to create, generate, test and evaluate models for the master's thesis at the University of Inland Norway, written by Håkon Gropen and Nicolay Vallee. The code constitutes a complete pipeline, with the exception of the data itself.

## EODHD data

The data was retrieved from the EODHD API with the *All-In-One* subscription (https://eodhd.com/pricing), where a personal/commercial license is required to reproduce our results.

## Python (Data extraction and transformation)

The Jupyter notebook contains code that parses and transforms data to be fed into statistical models. The term "statistical models" is here unrelated to the context of the master's thesis, and is used broadly to unite all predictive and/or inferential models (e.g. regression, PCA, classifiers, neural nets, etc.) under one category.

The process can be characterized as extract-transform-load:
Parse and query JSON data from the API $\rightarrow$ Transform and clean the data into useful time-series features in their respective data frames.

## R (Modeling)

There is some overlap with the data transformation step here: the data model imposes a structure designed to maintain integrity and keep the models operable. For example, for the iterated WLS regressions, it is much easier to load 12 time-series features and turn them into 1 707 cross-sections in memory, rather than creating 1 707 separate cross-sections as individual files.

Other than that, the R code includes WLS regressions, SVD-based PCA, model-specific exponential weighting schemes, hypothesis tests, plots and descriptive statistics. The descriptive statistics were mainly used to monitor and evaluate the integrity of model construction and hypothesis tests.

## Extended information

Extensive information regarding the data and model construction can be found in the main master's thesis document.
