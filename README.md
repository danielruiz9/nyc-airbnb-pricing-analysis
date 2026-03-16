# NYC Airbnb Pricing Inefficiency & Reviews

## Overview
This project asks whether more frequent Airbnb review activity is associated with lower pricing inefficiency in New York City listings.

Instead of modeling price directly, I define **pricing inefficiency** as the absolute deviation between a listing’s price and the median price of similar listings in the same **neighbourhood × room type** group. I then test whether listings with higher **reviews per month** tend to be priced closer to that local benchmark.

The project also examines whether this relationship depends on the clarity of local market signals, proxied by the density of comparable listings.

## Research Question
To what extent is review intensity (`reviews_per_month`) associated with lower pricing inefficiency, and is this relationship stronger in markets with clearer price signals? 

## Data
The analysis uses NYC Airbnb listing data as the main dataset, merged with:
- **NYPD complaint data** (borough-level crime controls)
- **MTA subway station data** (nearest-subway accessibility)
- **MODZCTA geographic boundaries** for spatial aggregation and mapping

The final working sample contains **38,726 listings** after cleaning and trimming. 

## Methods
- Cleaned and prepared Airbnb listing data in **Python**
- Constructed a listing-level **pricing inefficiency** metric
- Built a comparable-listing density measure within `neighbourhood × room_type`
- Merged external crime and transit datasets
- Used **GeoPandas** for spatial joins and nearest-subway calculations
- Produced **choropleth maps** by MODZCTA
- Estimated **OLS regressions with robust standard errors** to test the review–mispricing relationship 

## Key Findings
- Listings with higher **reviews per month** tend to have **lower pricing inefficiency** on average.
- This relationship is **statistically significant but economically modest**.
- The negative review–mispricing relationship appears **weaker, not stronger, in denser comparable markets**, contrary to the original mechanism hypothesis. 

## Spatial Component
The project includes spatial analysis and mapping of:
- mean absolute mispricing
- mean reviews per month
- mean comparable-listing density
- mean distance to nearest subway station

These maps show meaningful geographic variation across NYC and help motivate the regression analysis. 

## Tools Used
- Python
- pandas
- numpy
- matplotlib
- GeoPandas
- statsmodels
- Stargazer

## Notes
This project is descriptive rather than causal. Pricing inefficiency is defined relative to a local benchmark, and the analysis is intended to study patterns in host pricing behavior rather than identify causal effects. 
