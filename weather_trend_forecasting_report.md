
# Global Weather Trend Forecasting and Climate Pattern Analysis

## PM Accelerator Mission
Product Manager Accelerator is designed to support product management professionals through every stage of their careers, helping aspiring and experienced PMs build skills, prepare for interviews, and transition into product roles.

## Project Objective
This project analyzes the Global Weather Repository dataset to identify weather trends, detect anomalies, compare forecasting models, and study relationships between weather, geography, and air quality.

## Dataset
The dataset contains daily weather observations for cities around the world with temperature, precipitation, humidity, wind, pressure, visibility, UV index, air quality, astronomy, and geographic features.

## Data Cleaning
Missing numeric values were replaced using median imputation. Missing categorical values were replaced with Unknown. Duplicate rows were removed. The last_updated field was converted into datetime format and used to create date, year, month, day, weekday, and day-of-year features for time-based analysis.

## Exploratory Data Analysis
The analysis showed global trends in average temperature and precipitation over time. Country-level summaries highlighted geographic variation in temperature, precipitation, humidity, and air quality.

## Anomaly Detection
Isolation Forest was used to detect unusual weather observations based on temperature, humidity, precipitation, pressure, wind speed, PM2.5, and PM10. These anomalies represent unusual combinations of weather and air quality conditions.

## Forecasting Models
The project compared Linear Regression, Ridge Regression, Random Forest, Gradient Boosting, and an ensemble model. The models were evaluated using MAE, RMSE, and R2.

## Best Model
The best-performing model based on RMSE was Random Forest.

## Model Results
| Model             |      MAE |     RMSE |       R2 |
|:------------------|---------:|---------:|---------:|
| Random Forest     | 0.177949 | 0.450415 | 0.998255 |
| Gradient Boosting | 0.331727 | 0.559389 | 0.997308 |
| Ensemble Model    | 0.418392 | 0.629441 | 0.996591 |
| Linear Regression | 0.940943 | 1.26474  | 0.986238 |
| Ridge Regression  | 0.94182  | 1.27809  | 0.985945 |

## Feature Importance
Permutation importance was used to identify which features most influenced temperature forecasting. The most important features were:

| feature            |   importance |
|:-------------------|-------------:|
| feels_like_celsius |   14.6471    |
| humidity           |    0.873067  |
| wind_mph           |    0.250792  |
| wind_kph           |    0.232291  |
| latitude           |    0.0181671 |
| gust_mph           |    0.0178964 |
| uv_index           |    0.0178386 |
| gust_kph           |    0.0177863 |
| longitude          |    0.0172722 |
| pressure_in        |    0.0109575 |

## Climate and Spatial Analysis
Spatial analysis showed that temperature and precipitation vary strongly by latitude, longitude, and country. Warmer regions generally appear closer to tropical latitudes, while precipitation varies by regional climate and local weather systems.

## Environmental Impact Analysis
Air quality variables such as PM2.5, PM10, ozone, carbon monoxide, nitrogen dioxide, and sulphur dioxide were compared with weather parameters. This helped evaluate how atmospheric and weather conditions relate to pollution patterns.

## Conclusion
This project demonstrates basic and advanced data science skills through data cleaning, EDA, anomaly detection, forecasting, ensemble modeling, feature importance analysis, air quality analysis, and spatial climate visualization.
