# Bitcoin-Price-Predictor

# Parser:
Use Pyspark to aggregate parsed block data into two files. 
transaction.csv: transaction related data
Address.csv: input, output transaction time, transaction volume and stuff

# Feature Engineering:
Future price: Price of the next interval. 

Transaction-related features: Aggregate data by timestamp to calculate, min, max volume, min max prices as well

Address related: Number of new traders in Bitcoin. Join payer, payee address and their occuring timestamp. Then we can join the table containing trader information to the earliest time they appear and then aggregate the number of new traders.

Join the temporary tables into new table. So that we have Index, Date, Open, High, Low, Close, Total Transaction Volume, Mean Degree, Number of New Addresses, Number of Transactions, Mean Transaction Value, Max Transaction Value, Min Transaction Value, Future Price. 

# ML:
Generalized linear model: Used when our model is not normally distributed.

Linear Regression model:  Easy to use and easy to run

Decision Tree:  In each internal node, look at some of the feature of sample, and in the last classify this sample. Good at interpretation and visualization. The key is how to select a good splitting criteria.  Sensitive to the depth of the tree.

Random forest: Ensembled of weak learners. Have a collection of decisio tree, each tree is trained with a subset of our sample. Not sensitive as single decision tree. But could be too general. 


# Metrics:
RMSE: Square root of MSE. Easier to diffretiate

MAE: Avg of abs differences

MSE: Average of squared errors.  Penalizes the large prediction errors. 

R2: Is used to determine number of independent variables in model. R2 percent of the variation in the data is explained by the y/x relationship

# Result:
Generalized linear model work to be the best, decision tree the worst. Because tree models are sensitive to noise in data. Since time-interval is small, 

For the linear model, we found that RMSE around 64, r2 around 1. RMSE around 64. We might say that this is because inaccuracy might be show n in Bitcoin transactions. We used centralized app to do so.
