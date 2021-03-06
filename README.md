# Home Buying


![photo](https://github.com/KaylaBolden/Home-Buying/blob/main/Screenshots/new_home_construction.jpg)

# Objective 
The housing market is nutoriouosly inefficient. Identifying the true value of a home compared to the price gives us an opportunity to use this inefficiency to our advantage. The goal is to build an algorythm that can identify how much a house is worth so that we can find opportunities for arbitrage when a home hits the market below its worth. If we can move fast enough via web scrapping thousands of for sale records and generating this output, we may be able make money before other bidders drive up the price.


 # Used tools 
  Programs: 

      1. Jupiter - python
      2. Tableau
      3. Powerpoint

  Methods:

      1. Linear Regression
      2. Random Forest
      3. Neural Networks
      4. Web Scrapping
      5. API Connection 
      2. Histograms, distribution plots, heat maps, box-whisker plots, bar plots, Chi squared testing, Hyperparameter tuning

  Libraries:

      1. Normalizer
      2. StandardScaler
      3. Min Max Scaler
      4. math
      5. statistics 
      6. matplotlib.pyplot
      7. seaborn
      8. statsmodels.api
      9. train_test_split
      10. one hot encoder
      11. numpy
      12. pandas
      13. statsmodels.formula.api
      14. linear_model
      15. is_numeric_dtype
      16. Redfin
      17. scipy
      18. requests
      19. urllib.parse
      20. chi2_contingency
      21. DBSCAN
      22. LinearRegression
      23. sklearn.metrics
      24. sklearn.feature_selection
      25. sklearn.linear_model
      26. mean_squared_error
      27. r2_score
      28. mean_absolute_error
      29. statsmodels.api 
      30. tensorflow
      31. train_test_split
      32. RandomForestRegressor
      33. make_regression
      34. variance_inflation_factor
      35. GridSearchCV
      36. sklearn.decomposition.PCA

 # Workflow
      1. Gather the Data 
      2. Explore the Data 
      3. Dealing with Nulls 
      4. Clean the Data 
          a. Categorical data: 
            i. needs to be grouped into fewer buckets
            ii. dropped if there are too many instances
            iii. cleaned if there are various values with the same meaning 
          b. Numerical data: 
            i. needs to be converted to number if object (may require functions for data transformations)
      5. Dealing with Outliers 
      6. Transform numerical columns to conform to a more normal standard distribution
      7. Check Multicollinearity
          a. Numeric- VIF and correlation matrix
          b. Categorical - chi squared testing
      8. Normalize, Min-max, or standardize the data 
      9. Build Clusters using DBScan
      10. Apply Train-Test Split 
      11. Hyoerparameter tuning for feature selection
      12. Train and Test random forest (since extra features don't hinder the model)
      12. Remove extra features based on feature importance
      11. Train Model Linear and Neural Network models
      12. Test Model Linear and Neural Network models

# Transformations
    Tested a variety of methods to convert my continuos variables into normal distributions:
    1. log
    2. square root
    3. square
    4. cubed 

Transformation | Numerical Factor
------------- | -------------
sqrt | totalfavoritescount
sqrt | taxesdue
sqrt | publicschoolrate
sqrt | basement_square_feet
sqrt | land_square_footage
sqrt | acres
sqrt | taxrate
sqr | totalamenities
none | latitude
none | longitude
none | daysonmarket
none | publicstudentteacherratio
none | publicstudentcnt
none | privatestudentcnt
log | squarefeet
log | viewcount
log | totaltourcount
log | privaterate
log | garage_parking_square_feet
cbd | yearbuilt
cbd | yearrenovated

# Scaling
    Tested a variety of scaling methods:
      1. Normalizer
      2. Standard Scaler
      3. Min ??? Max Scaler

# Feature Importance:
    
Feature | Regression P-Val | Random Forest Feature Importance
------------- | ------------- | -------------
daysonmarket | 0.518 | 0.00592214
publicstudentteacherratio | 0.344 | 0.004352648
publicstudentcnt | 0.946 | 0.005487916
privatestudentcnt | 0.385 | 0.006992907
squarefeet | 0 | 0.02421013
totaltourcount | 0.161 | 0.001894489
privaterate | 0.128 | 0.005642923
garage_parking_square_feet | 0.009 | 0.0081063
totalfavoritescount | 0 | 0.008720093
publicschoolrate | 0.001 | 0.006671266
basement_square_feet | 0.038 | 0.001758376
land_square_footage | 0.002 | 0.01105095
acres | 0.319 | 0.02747586
taxrate | 0 | 0.04166951
totalamenities | 0.488 | 0.005520898
x2_Condo&Manufactured | 0.19 | 0.002256557
x2_Multi-Family | 0.195 | 0.001505547
Foundation_Continuous Footing | 0 | 0.02464942
Foundation_other | 0 | 0.007086104
Garage_Finished | 0.02 | 0.002233992
Garage_other | 0.328 | 0.00693243
Building_Quality_0 | 0 | 0.4383543
Building Quality_3 | 0 | 0.08868372
Walls_0 | 0.005 | 0.002632515
Walls_1 | 0.006 | 0.004978199
Walls_4 | 0 | 0.007193782
Roof_0 | 0.065 | 0.06866194
Roof_1 | 0 | 0.005233747
Roof_2 | 0 | 0.006545969
Roof_3 | 0 | 0.1469811
Location_2 | 0.068 | 0.00129702


    Out of all the methods, Random Forest and Min-max scaler produced the highest accuracy:
![photo](https://github.com/KaylaBolden/Home-Buying/blob/main/Screenshots/Picture1.png)

# Results and conlusions 
      The accuracy of the random forest model on test set is: 44,124 and on the for sale set is: 50,423. Assuming there is no difference between the homes in the two sets, it stands to reason the additional discrepenct from test to sale is the market inefficiency.
![photo](https://github.com/KaylaBolden/Home-Buying/tree/main/Screenshots)

## Dataset

The dataset after gathering the data is [**finalDatecsv**](https://github.com/KaylaBolden/Home-Buying/blob/main/finalData.csv).
The dataset after all cleaning and including all the models' predictions is [**withpredictions.xlsx**](https://github.com/KaylaBolden/Home-Buying/blob/main/withpredictions.xlsx).

This data set includes:

1. **Home Buying** data:

    |   |   |
    |---|---|
    |daysonmarket | basement_square_feet | Building_Quality_0
    |publicstudentteacherratio | land_square_footage | Building Quality_3
    |publicstudentcnt | acres | Walls_0
    |privatestudentcnt | taxrate | Walls_1
    |squarefeet | totalamenities | Walls_4
    |totaltourcount | x2_Condo&Manufactured | Roof_0
    |privaterate | x2_Multi-Family | Roof_1
    |garage_parking_square_feet | Foundation_Continuous Footing | Roof_2
    |totalfavoritescount | Foundation_other | Roof_3
    |publicschoolrate | Garage_Finished | Location_2
    |||


# Tableau
A full analysis with visuals breaking down key drivers of home value can be found in [**Home Buying**](https://public.tableau.com/views/HomeBuying_16452186025640/TotalViews?:language=en-US&:display_count=n&:origin=viz_share_link). 

# Presentation
A powerpoint containing the agenda and tying it all together can be found in [**Home Buying.pptx**](https://github.com/KaylaBolden/Home-Buying/blob/main/Home%20Buying.pptx). 

# Jupyter Notebook
A python code for data gathering can be found in [**Data Gathering.ipynb**](https://github.com/KaylaBolden/Home-Buying/blob/main/Data%20Gathering.ipynb). 
A python code for the analysis can be found in [**Home-buying-Analysis.ipynb**](https://github.com/KaylaBolden/Home-Buying/blob/main/Home-buying-Analysis.ipynb). 
