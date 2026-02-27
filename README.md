# NYC Airbnb Pricing Inefficiency & Reviews (ECO225)

## Overview
This project analyzes NYC Airbnb listings to examine whether listings with higher review intensity (reviews_per_month) tend to be priced closer to neighbourhood-specific market benchmarks ("mispricing").

## Research Question
Do listings with more reviews per month appear to be priced closer to local medians within their neighbourhood × room type category?

## Key Variables Constructed
- **mispricing_abs** = | price − median(price) within (neighbourhood, room_type) |
- **comp_density_log** = log(1 + number of comparable listings in neighbourhood × room_type)
- **reviews_per_month** used as a demand/review intensity proxy

## Method
- Cleaned and filtered NYC Airbnb data in Python (pandas).
- Engineered pricing deviation and competition density measures.
- Merged borough-level controls.
- Conducted exploratory analysis using summary tables and visualizations.

## Files
- `project_analysis.html` — full analysis notebook (rendered with outputs)

## Tools Used
Python, Jupyter Notebook
