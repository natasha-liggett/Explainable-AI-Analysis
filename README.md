# Explainable-AI-Analysis Overview
I cannot release the data used for the analysis or the full analysis as it has not yet been published. ExplainableAI_Excerpt.Rmd contains the base of the explainable AI analysis including building and tuning the hyperparameters for the base learners, building a stack ensemble model, and conducting a basic feature importance analysis.

## Data

### Environment Data
- The weather dataset used to construct the environmental variables contains over 12 million observations of daily weather for the past 50 years in locations around the world. 15 different weather measurements are included. 
- Environmental variables like phototermal quotient, photothermal reduction factor, daily thermal time, and more were calculated or modeled using the weather data.
- Weather data was joined to crop yield data by latitude / longitude.

### Crop data
- Over 220k observations from locations around the world. Crop yields from multiple observations in the same location and year are averaged.
- Data spans a 50 year period. Not every location is represented each year. 
- Includes data such as crop yield and information on key dates in the growth cycle.
- Environmental variables are averaged over key periods in the growth cycles

## Analysis
- 4 base learners are integrated to create the stack ensemble model
  - Base models: KNN model, Ranger model, XGboost model, and elastic net model
- Feature importance determined with a loss reduction analysis
