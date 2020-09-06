# Taxi-demand-prediction

Dataset: https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Problem statement taken: Predict number of Taxi required for a given location and for a given time

#time_series_analysis #Machine_learning #LSTM #Data_manipulation #Preprocessing #EDA #Visualization #Geotagging

================================================================================================================================================

### Problem Statement Formed

* Find the number of pickups avaliable in next 10 minute given a region

### Use case:

* This details can be used regulate the Cabs to particaluer region based on demand (Number of pickups avaliable) in that region

### Bussiness Impact

* In this way the resource utilization (cabs/taxi) can be optimized


### Data Cleaning

* Univariate analysis is done on each features and ouliers are removed in the dataset.

* Since data size is large (12.3 million datapoints) better gone with removing outliers instead of other techniques like mean/median imputations

### Data modelling

* Data at hand don't have region and number of pickups happend for each ten minutes

* Clustering algorithm is applied to cluster the entire Newyork into 40 regions (based on problem at hand)

* Then time bins (10 min bin) are created

* At certain points in time (some 10 min interval) no pickus happned. For time series continuity smoothing operation is applied

### Algorithm Applied

* Unsupervised : Clustering --> Kmeans 

* Supervised : Machine learning --> LinearRegression, RandomforestRegression, XGboost_regression 

* Tuning : Grid Search, Random Search

* Supervised : Deep learning --> MuliLayerPerceptron, LSTM

### Feature Engineering

* Fourier transformation
* Simple exponential smoothing
* Double exponential smoothing
