# Putting Machine Learning into Production
## Intro

 > MLOps is a set of best practices for putting machine learning into production
 
A taxi service may want to develop a system that predicts the length of a ride in minutes based on the pickup
and drop-off locations, and make it available to its customers via an application.

Several steps are involved in deploying such a service:
1. __design:__ evaluate whether ML is the appropriate approach
2. __model training:__ run experiments to find the best model
3. __operation:__ make the model available to new inputs as a service

MLOps helps in all stages of machine learning deployment by enabling automation, collaboration, and monitoring.

## Overview
Training a machine learning model is a non-linear process that involves trial-and-error experimentation.
Data scientists and developers often train and compare different models and adjust parameters in search
of the optimal combination.

MLOps makes use of several tools that ensure experiments are documented and reproducible. 
An _experiment tracker_ logs model parameters and associated metrics, preserving the entire history of experiments.
The _model registry_ saves models and enables versioning and comparing models.

One a model has been selected, the workflow from raw data to inputs must be modularized into a ML pipeline
that can be executed using new data to generate predictions

Finally, the model must be placed in an accessible service.


## Maturity Model
MLOps covers a wide range of tools and best practices that an organization may adopt for developing
machine learning systems. Rather than an all-or-nothing decision, an organization must settle on a level of adoption
that is most beneficial given its current needs and resources.

The MLOps Maturity Model defines 6 levels technical capability, which takes into account culture, process, and
technology at hand.

### 0. No MLOps
- no automation
- all code lives in jupyter notebooks
- no collaboration, cumbersome hand-overs
### 1. DevOps, No MLOps
- developers assist data scientists with model deployment
- CI/CD, unit tests, integration tests
- releases are automated, but not ML-specific
- data scientists are still separated from engineers
### 2. Automated Training
- parametrized pipeline in the form of a script
- experiment tracking and model registry
- deployment may not be automated
- integrated data scients/engineering teams
### 3. Automated Deployment
- low-friction model deployment
- API calls to an ML platforms
- A/B tests for comparing models
### 4. Full MLOps Automation
- fully automated deployment
- near zero-downtime system
- centralized metrics