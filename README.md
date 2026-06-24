# Master's Thesis: Financial Risk-Factor Modeling: A comparison of Characteristic and Statistical risk-factor models for forecasting portfolio risk in Norway

This repository contains all code used to create, generate, test and evaluate models for the master's thesis at University of Inland Norway created by Håkon Gropen and Nicolay Vallee. All code includes a complete pipeline, with the exception of the data itself.

## EODHD data

The data was retrieved from EODHD API with the *All-In-One* subcription (https://eodhd.com/pricing), where a personal/commerical license is required to be able to reproduce our results. 

## Python (Data extraction and transformation)

The jupyternotebook contains code that parses and transforms data to be fed in to statistical models at-the-ready. The use of the term "statistical models" is unrelated to the context of the master's thesis, and is a broad term used to unite all predictive and/or inferential models (e.g. regression, PCA, classifiers, Neural Nets, etc.) under one category. 

The process can be characterized extract-transform-load-
Parse and query JSON data from API $\rightarrow$ Transform and clean data to useful time-series features into respective data-frames. $\rightarrow$ Clean 

## R (Modeling)

There is somewhat overlap from data transformation here, where the necessary alterations regarding data modeling force structure that aims to maintain integrity and model operatability. For example, for the iterated WLS-regressions, it is much easier to load 12 time-series features and turn them into 1 756 cross-sections in program rather, than creating 1 756 seperate cross-sections as individual files. 

Other than that, the R-code includes WLS-regressions, SVD-based PCA, model specific exponential weighting schemes, hypothesis tests, plots and descriptive statistics. The descriptive statistics were mainly used to monitor and evaluate the integrity of model construction and hypothesis tests.
