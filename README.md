# Vessel Loitering Prediction

A machine learning project to predict extended vessel loitering events (>24 hours) based on historical vessel behavior, port factors, and weather conditions.

## Project Overview

### Research Questions

**Main Question:**
Can we predict whether a vessel will engage in extended loitering (>24 hours) during its next shipment based on historical vessel behaviour, port factors, and weather conditions?

**Sub-questions:**
1. Which factors (vessel behaviour, weather patterns, or port congestion) are most predictive of extended loitering events?
2. How does prediction accuracy vary across different geographical regions and seasons?
3. What is the minimum amount of data on a vessel or port to make reliable loitering predictions?

### Hypotheses

- Vessels with irregular or inconsistent historical port visit patterns will show higher likelihood of extended loitering events
- Seasonal patterns will be significant predictors, with higher likelihood of extended loitering during peak shipping seasons and major holiday periods

### Project Contribution

**Prof feedback: "Need to show more clearly what this prediction could be used for. Will we save time, money? Go further into cost-benefit analysis."**
- Builds on existing arrival prediction models with loitering-specific insights
  - Development of new features capturing vessel behavior patterns
- Practical applications for: 
  - Proactive port capacity management
  - Early warning system for supply chain disruptions
  - Data-driven vessel scheduling optimization

## Methodology

### Data Preprocessing

1. Clean and combine vessel, port, and weather data using timestamp matching
2. Engineer features from historical vessel behaviour patterns
3. Create port congestion proxies from available port data

### Model Development

1. Split data into training and testing sets (80-20), following temporal order
2. Develop and compare multiple models:
   - Logistic regression (baseline)
   - Decision Tree
   - Random Forest
   - Gradient Boosting
3. Model Selection and Optimization:
   - Select best performing model based on prediction accuracy and interpretability
   - Optimize hyperparameters using cross-validation
   - Evaluate model robustness across different regions and time periods

## Data Sources

### Port and Vessel Data
- Source: Global Fishing Watch
- Period: January 2017 to October 2024
- Number of observations: ~718,960
- Key Variables (36 total):
  - Vessel characteristics
  - Historical loitering events
  - Port information and events
  - Vessel authorization status and regional information

### Weather Data
- Source: Open-Meteo
- Period: January 2017 to October 2024
- Frequency: 1-hour
- Key Variables (32 total):
  - Geographic Location and Timestamp
  - Temperature
  - Wind speed and direction
  - Precipitation and visibility
  - Cloud coverage

## Project Context

Recent events highlight the importance of this research:
- In September 2021, a record 73 cargo ships were anchored outside Los Angeles and Long Beach ports, compared to just 1 ship in pre-pandemic times
- Container shipping cost rates surged 256% to Europe since December 2023 (UNCTAD, 2024)
- Vessel loitering has led to "up to 70% rise in greenhouse gas emissions" for major shipping routes

### Impact
- Higher freight rates will affect consumer prices within a year
- Supply chain delays drive inflation and product shortages
- Significant environmental impact from increased emissions
