# Restaurant Revenue Prediction 

As part of a course final project, I cleaned and analyzed a set of dataset(s), both the training set and the test set, that contained restaurant information used to predict the potential revenue through a linear regression. 

Beginning with the information provided by <a href="https://www.kaggle.com/c/restaurant-revenue-prediction/data">Kaggle</a>, the training set was explored to see what kind of insights were provided. 

<p align="center">
  <img src="https://github.com/lherna/restaurant_revenue_prediction/blob/main/img/RR_prob.png" title="rr_intro">
</p>

Signaling the data to be pretty much localized to the Turkey region, I went ahead and went a little deeper in the exploration to see if there were any interesting insights that could be unraveled as to the concentration of these restaurants. 

<p align="center">
  <img src="https://github.com/lherna/restaurant_revenue_prediction/blob/main/img/restaurant_region.png" title="loc_region">
</p>

Seeing that there was indeed some indication to the Istanbul metropolitan region, the next thing I wanted to see was whether the restaurant "Type" provided in the dataset differed. 

<p align="center">
  <img src="https://github.com/lherna/restaurant_revenue_prediction/blob/main/img/restaurant_type.png" title="rtype">
</p>

After noticing that there was a missing category within this feature, specifically the "MB" or "Mobile" type, it came to mind that the test set had to be modified to accomodate for this through an imputation method via a KNN (Imputer) available through sci-kit learn.

Preparing this along with the remaining category variables to be replaced by a numerical variable via a dummy variable, the data was processed as shown in the <a href = "https://github.com/lherna/restaurant_revenue_prediction/blob/main/PHYS247_Final-Restaurant_Revenue_Prediction.ipynb">Jupyter Notebook</a> in this repository. 

Leaving out the "City" feature due to the amount of categorical variables that would have to have been converted in addition to the already excessive amount of features, the pre-processed data was then further handled to be normalized using sci-kit learn's StandardScaler in preparation for the PCA (Principal Component Analysis) in order to see if the amount of features could be reduced. 

Noticing a difference from the unprocessed data to the processed data, the linear regression gave clear results to the predicting capabilities with respect to this data: 

<p align="center">
  <img src="https://github.com/lherna/restaurant_revenue_prediction/blob/main/img/restaurant_region.png" title="soln">
</p>









