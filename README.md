# Home-Buying


![photo](https://github.com/KaylaBolden/Home-Buying)

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
      5. math
      6. statistics 
      7. matplotlib.pyplot
      8. seaborn
      9. statsmodels.api
      10. train_test_split
      11. one hot encoder
      12. numpy
      13. pandas
      14. statsmodels.formula.api
      15. linear_model
      16. is_numeric_dtype
      17. Redfin
      scipy
      requests
      urllib.parse
      chi2_contingency
      DBSCAN
      LinearRegression
      sklearn.metrics
      sklearn.feature_selection
      sklearn.linear_model
      mean_squared_error
      r2_score
      mean_absolute_error
      statsmodels.api 
      tensorflow
      train_test_split
      RandomForestRegressor
      make_regression
      variance_inflation_factor
      GridSearchCV
      sklearn.decomposition.PCA

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

    Attempt | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
Seconds | 301 | 283 | 290 | 286 | 289 | 285 | 287 | 287 | 272 | 276 | 269

# Scaling and Balancing data

    Tested a variety of scaling methods:
      1. Normalizer
      2. Standard Scaler
      3. Min – Max Scaler

    Tested multiple data balancing methods:
      1. Random Over Sampling
      2. Random Under Sampling
      3. SMOTE
      4. Tomeklinks

    Out of all the methods, standard scaler and Random over Sampling preoduced the highest ROC-AUC and Kappa scores:
![photo](https://github.com/KaylaBolden/data_mid_bootcamp_project_classification/blob/master/table.png)

# Results and conlusions 
      The accuracy of the model on test set is: 0.70 and the Kappa of the model is: 0.41. The ROC-AUC is 77%
![photo](https://github.com/KaylaBolden/data_mid_bootcamp_project_classification/blob/master/Screen%20Shot%202021-12-04%20at%204.51.05%20PM.png)


## Dataset

The dataset provided [**creditcardmarketing.csv**](https://github.com/KaylaBolden/data_mid_bootcamp_project_classification/blob/master/creditcardmarketing.csv) 


This data set includes:

1. **CreditCardMarketing** data:

    |   |   |
    |---|---|
    |  Customer Number | Offer Accepted   |
    | Mailer Type  | Income Level  |
    | Bank Accounts Open  |  Overdraft Protection |
    |  Credit Rating | Credit Cards Held  |
    | Homes Owned|Household Size|
    | Own Your Home|Average Balance|
    | Balance||
    |||


# SQL
The dataset provided [**Classisfication Model.sql**](https://github.com/KaylaBolden/data_mid_bootcamp_project_classification/blob/master/Classisfication%20Model.sql). 

# Tableau
A full analysis with visuals breaking down key drivers and customer demographic profiles can be found in [**Credit Card Offers.twbx**](https://github.com/KaylaBolden/data_mid_bootcamp_project_classification/blob/master/Credit%20Card%20Offers.twbx). 

# Presentation
A powerpoint containing the agenda and tying it all together can be found in [**Offer Acceptance Slides.pptx**](https://github.com/KaylaBolden/data_mid_bootcamp_project_classification/blob/master/Offer%20Acceptance%20Slides.pptx). 
