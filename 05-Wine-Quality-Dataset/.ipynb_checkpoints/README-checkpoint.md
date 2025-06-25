# **Wine Quality Dataset Analysis and EDA**

## EDA Questions:
- Q1: What chemical characteristics are most important in predicting the quality of wine?
- Q2: Is a certain type of wine (red or white) associated with higher quality?
- Q3: Do wines with higher alcoholic content receive better ratings?
- Q4: Do sweeter wines (more residual sugar) receive better ratings?
- Q5: What level of acidity (pH) is associated with the highest quality?


## Data Wrangling:
Our data can be found on `wineQualityReds.csv` and `wineQualityWhites.csv` files provided on this repository, 
downloaded from [Kaggle](https://www.kaggle.com/datasets/danielpanizzo/wine-quality) 
and originaly from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wine+Quality). 


## Data Cleaning:
### Exploration Summery
- red dataframe consists of 1599 records and 13 attributes, while white dataframe consists of 4898 records and the same attributes.
- both data frames has no NaNs nor duplicated values.
- we woul combine the two dataframes and append a new categorical column to indecate the wine color for better analysis.
- columns data types are consistant.
- `Unnamed: 0` column would be dropped.

We endded up with with 13 columns and 6497 rows for our data to begin the analysis with. 
a new csv file containing our full data is saved in `wine_full.csv`.


## Data Visualization
Using `Matplotlib` and `Seaborn`, we made several meaningful visuals and charts to help us gain informative insights regarding any correlation between attributes in our dataset, that'll be discussed in the next section.


## Conclusion
These are derived conclusions after completing our data visualisation phase.

### Q1: What chemical characteristics are most important in predicting the quality of wine?
- the vast majority of the wine has a `quality` of 6, while less numbers has a `quality` of 9.
- using correlation plot, we can easily see if certain attributes are correlated more strongly to wine `quality` than some others.

  - strong correlated attributes:
    - `alcohol` and `quality`, and it's clear that this is the highest relation that affects wine `quality`.
  - weak correlated attributes (do not depend on each other):
    - `density` and `alcohol`.
    - `free.sulphur.dioxide` and `citric.acid` has almost no correlation with quality
  - `density` has strong positive correlation with `residual.sugar` and strong negative correlation with `alcohol`.

---
### Q2: Is a certain type of wine (red or white) associated with higher quality?
- there is noticable deviation between `white` and `red` wine counts.
- `white` wine formes the vast majority of our dataset as it appears in more than 75% of the times.
- most of the `white` wine has a `quality` of 6, while most of the `red` wine has a `quality` of 5.
- the mean `quality` of `red` and `white` wine are ve`ry close.
- `white` wine has the best mean `quality` higher than `red` wine.

---
### Q3: Do wines with higher alcoholic content receive better ratings?
- we have the highst `alcohol` content at 14.9.
- most of the wine has `alcoholic` content around 10.4.
- most of our dataset that has a `quality` of 6 appears to have relatively low `acoholic` content, but it's still above the mean.
- high `alcoholic` content only appears in our dataset with high `quality` wine.

---
### Q4: Do sweeter wines (more residual sugar) receive better ratings?
- we can see that the highest `sugar` content is tied to a `quality` of 5, while lower `sugar` content appears to have respectively higher `quality`.

---
### Q5: What level of acidity (pH) is associated with the highest quality?
- most of the wine in our dataset has high `acidity level`
- it's clear that all four acidity levels has close mean `quality`, but the `Low acidity` level has the highest `quality` in our dataset.


## Built with:		
- JupyterLab	
- Python3	   	
- Pandas		
- Numpy			
- Matplotlib	
- Seaborn		
