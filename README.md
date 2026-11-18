# Spatial Ecology

## Overview

Spatial ecology studies the **dynamic** patterns of a specific **species** during a particular **time** period within **regions** of interest. It combines a spatial dimension (longitude and latitude coordinates) with a temporal one, usually based on the life cycle of the species (a one-year cycle is often used).

This workshop introduces the two main families of models used in the field, mechanistic and statistical, and ends with a hands-on activity in R: predicting the severity of mountain pine beetle infestation in a lodgepole pine area in 2014 using data from 2007 to 2013.

- **Workshop lead:** Xiaoqi Xie
- **Date:** November 20, 2026
- **Location:** 550 Sherbrooke Street, Montreal, Quebec
- **Contact:** [workshop-micm@mcgill.ca](mailto:workshop-micm@mcgill.ca)

## Requirements

### Knowledge

- Basic familiarity with R (running scripts, loading packages, working with data frames)
- Introductory statistics, including linear regression

### Computational

- A laptop with R and RStudio installed (see below)
- No unix terminal is needed; all analyses are run in R

### Software

- [R](https://cran.r-project.org/)
- [RStudio Desktop](https://posit.co/download/rstudio-desktop/)
- Needed R libraries and their installation code can be found in the script.

## Small Outline/Structure

- **Introduction**
  - What spatial ecology studies: species, time, and regions of interest
  - Spatial and temporal dimensions of the data
- **Method**
  - Mechanistic models: ordinary (ODEs), partial (PDEs), and stochastic (SDEs) differential equations
    - Example: the Lotka-Volterra predator-prey model
    - Strength: reliable long-term predictions
  - Statistical models: regression models and machine learning models
    - Example: linear regression of yearly bee counts on temperature
    - Strength: reliable short-term predictions, useful for natural resource managers planning the next five or ten years
  - Time-series analysis
- **Hands-on activity**
  - What do we study? The mountain pine beetle (MPB; *Dendroctonus ponderosae*), its one-year life cycle, and its primary host, lodgepole pine
  - How to study? A zero-inflated negative binomial (ZINB) model
    - Response: number of infested trees in the current year
    - Climatic covariates: relative humidity, wind speed, soil moisture index, degree days, overwinter survival probability
    - Ecological covariates: pine age, pine density, last year's infestations within the cell, weighted influence of last year's infestations within a 4 km radius excluding the cell
  - Severity classes per 500 m grid cell: no infestation (0 trees), light (1-3), moderate (4-25), very severe (>25)
  - Model evaluation: accuracy and root mean square error (RMSE)

## References

Amman, G. D. (1978). Biology, ecology, and causes of outbreaks of the mountain pine beetle in lodgepole pine forests. In A. A. Berryman, G. D. Amman, & R. W. Stark (Eds.), Proceedings: Theory and practice of mountain pine beetle management in lodgepole pine forests, April 25-27, 1978, Pullman, WA (pp. 39-53). University of Idaho, Forest, Wildlife and Range Experiment Station, Moscow, ID.

Safranyik, L., & Carroll, A. L. (2006). The biology and epidemiology of the mountain pine beetle in lodgepole pine forests. In L. Safranyik & B. Wilson (Eds.), The mountain pine beetle: A synthesis of biology, management, and impacts in lodgepole pine (pp. 3-66). Natural Resources Canada, Canadian Forest Service, Pacific Forestry Centre, Victoria, BC.
