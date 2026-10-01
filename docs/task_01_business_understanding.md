# Task 1: Business Understanding and Data Requirements

**BCG X Data Science Job Simulation on Forage - PowerCo churn case**

> **Simulation disclosure:** This document summarizes work completed as part of the BCG X Data Science Job Simulation on Forage. It is an educational job simulation and does not represent employment, an internship, or client work performed for BCG X or PowerCo.

## Business problem

In the simulation scenario, PowerCo is investigating customer churn in the SME segment and has proposed **price sensitivity** as a possible driver. The data-science objective is to test that hypothesis rather than assume it is true.

## Analytical question

How strongly is customer churn associated with pricing, and what other customer, consumption, contract, or product characteristics may help explain or predict churn?

## Data required

The analysis requires customer-level and pricing information that can be linked through the customer identifier, including:

- churn outcome
- customer activity and sales-channel information
- electricity and gas consumption
- contract activation, end, modification, and renewal dates
- forecast consumption and forecast price variables
- product and service indicators
- commercial margin and subscribed power measures
- monthly variable and fixed prices across off-peak, peak, and mid-peak periods

## Proposed approach

1. Validate data quality, coverage, types, and missing-value representations.
2. Explore churn prevalence and customer characteristics.
3. Compare pricing behavior between churned and retained customers.
4. Engineer features that capture price movement, customer tenure, usage, contract timing, and commercial value.
5. Train the Random Forest classifier specified in the simulation.
6. Evaluate the model with metrics appropriate for an imbalanced churn target, not accuracy alone.
7. Translate the findings into a concise stakeholder recommendation.

## Working hypothesis

Price sensitivity may contribute to churn, but the analysis should allow competing explanations to emerge from the data. The hypothesis is treated as a question to test, not a conclusion to prove.
