# Toronto Rentals Price Analysis & Prediction

This project analyzes rental listings in Toronto to understand what drives rent prices and predicts rent per square foot ($/sqft) using machine learning models.

It covers the end-to-end data science pipeline: data collection, cleaning, feature engineering, exploratory analysis, and modeling.

## Project Structure
```
toronto-rentals/
│── data/
│   ├── raw/          # raw CSVs (listings, subway stations, universities)
│   ├── interim/      # cleaned listings
│   └── processed/    # final dataset with features
│── notebooks/
│   ├── 01_collect_and_clean.ipynb
│   ├── 02_geocoding.ipynb
│   ├── 03_features_distances.ipynb
│   ├── 04_eda.ipynb
│   └── 05_modeling.ipynb
│── src/              # utility functions (cleaning, geocoding, feature engineering)
│── visuals/          # screenshots, folium maps
│── README.md
```
## Data Pipeline

1. ### Data Collection

 - ~100 rental listings manually collected.

 - Subway station + university data added from external sources.

2. ### Cleaning

 - Removed duplicates, fixed inconsistent formatting.

 - Outliers removed: rent < $1200, price_per_sqft < 2 or > 5.

3. ### Feature Engineering

 - price_per_sqft

 - bed_bath_ratio

 - Distance to nearest subway station

 - Distance to Union Station (downtown core)

 - Distance to nearest university

4. ### Exploratory Data Analysis (EDA)

 - Histograms, scatterplots, correlation heatmaps.

 - Grouped analysis by bedrooms & stations.

 - Geospatial visualizations with Folium maps.

## Key Insights

- Larger apartments → higher absolute rent, but lower $/sqft (discount effect).

- Location matters: closer to subway or Union Station → higher $/sqft.

- University proximity has weaker effect (local to student-heavy areas).

- Bedrooms/bathrooms add little once size is controlled for.

## Modeling
### Models tested

- Linear Regression

- Log-Linear Regression

- Random Forest Regressor

- Gradient Boosting
