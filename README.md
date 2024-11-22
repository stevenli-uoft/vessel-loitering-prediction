# Predicting Extended Fishing Vessel Loitering Events

## Overview
This research project aims to predict whether fishing vessels will engage in extended loitering events (>24 hours) during their next voyage based on historical vessel behavior, port factors, and weather conditions. By focusing on fishing vessels specifically, we seek to help fishing companies optimize their operations and prevent disruptions in the fish supply chain.

## Motivation & Benefits
Extended vessel loitering presents several challenges in the fishing industry:
- Increased fuel consumption and operational costs for fishing companies
- Disruptions to fish supply chains affecting market prices and availability
- Environmental impact through increased emissions during idle periods

Accurate prediction of extended loitering events can help:
- Reduce operational costs through better voyage planning
- Maintain more stable fish supply chains
- Lower environmental impact through reduced idle time
- Enable proactive resource allocation at ports

## Research Questions

### Main Question
Can we predict whether a fishing vessel will engage in extended loitering (>24 hours) during its next voyage based on historical vessel behaviour, port factors, and weather conditions?

### Sub-questions
1. Which factors (vessel behaviour, weather patterns, or port congestion) are most predictive of extended loitering events for fishing vessels?
2. How does prediction accuracy vary across different geographical regions and fishing seasons?
3. What is the minimum amount of data needed on a vessel or port to make reliable loitering predictions?

## Hypotheses
- Fishing vessels with irregular or inconsistent historical port visit patterns will show higher likelihood of extended loitering events
- Seasonal patterns will be significant predictors, with higher likelihood of extended loitering during peak fishing seasons and major holiday periods

## Data Sources

### Vessel & Port Data (Global Fishing Watch)
- Period: January 2017 to October 2024
- 36 variables including:
  - Vessel characteristics
  - Historical loitering events
  - Port information and events
  - Vessel authorization status
  - Regional information
- 718,960 observations

### Weather Data (Open-Meteo)
- Period: January 2017 to October 2024
- 32 variables including:
  - Geographic location and timestamp
  - Temperature
  - Wind speed and direction
  - Precipitation and visibility
  - Cloud coverage
- 1-hour frequency data

## Methodology

### Data Preprocessing
1. Clean and combine vessel, port, and weather data using timestamp matching
2. Engineer features from historical vessel behaviour patterns
3. Create port congestion proxies from available port data

### Model Development
1. Data Splitting
   - 80% training set
   - 20% testing set
   - Maintain temporal order

2. Model Comparison
   - Baseline: Logistic regression
   - Decision Tree
   - Random Forest
   - Gradient Boosting

3. Model Selection and Optimization
   - Select best performing model based on prediction accuracy and interpretability
   - Optimize hyperparameters using cross-validation
   - Evaluate model robustness across different regions and time periods

## Expected Contribution
- Development of new features capturing fishing vessel behavior patterns
- Insights into factors affecting fishing vessel loitering
- Practical applications for:
  - Proactive port capacity management
  - Early warning system for fish supply chain disruptions
  - Data-driven vessel scheduling optimization
