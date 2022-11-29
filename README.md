# Bitcoin-Price-Predictor

- Implemented standalone Bitcoin price predictor with PySpark framework and Docker that perform big data
analysis on server cluster.
- Processed raw Bitcoin block chain transaction histories with PySpark on server cluster setup with Docker.
Save pairs of transaction hash, transaction volume and output address in files.
- Use PySpark SQL library to clean, transform histories into training data set.
- Implemented regression model with PySpark MLlib library to predict future prices. Evaluate model
correctness with rase, mae, r2 and var metrices.
