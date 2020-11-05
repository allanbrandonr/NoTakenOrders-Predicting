# NoTakenOrders-Predicting
Fitting a model to predict no taken orders by couriers

# Summary

### Data 
Data quality was good in general
Duplicated values were dropped and the row with the most recent date was kept
Fraud suspected cases were dropped. Had total earnings greater than 8 times the average earnings value
I separated the data into training and testing sets with 80% and 20% of the orders respectively

### Over sampling
The proportion of non taken orders is small (7.8%) and could cause biased estimations 
because taken orders are over represented in the sample

I did a sampling with replacement of the non taken orders in the training set in order
to have a training set with 50% of non taken orders. Just on the training set.

Keep in mind that because of over sampling, probabilities estimated in the training set 
must be compared in relative terms tather than in absolute terms

### The model
I estimated a decision tree model. It is a fast computing and easy interpretable type of model 
convienient to be used in a first mvp.

I used the f1 score in order to select the best model. Optimizing on this score increases both 
the precision and the recall of a classifier. 

I may be conserned obout how does the model works on an out of time sample as if not 
done carefully, decision trees may overfit and lose prediction power.

Model has the best testing f1 score and not at all one of the highest training f1 scores. 
This helps to avoid overfitting on the training set.

The model is 185% better than a naïve estimator, which has testing f1 score of 8.08%

### Additional

Check the summary deck included for more detail



