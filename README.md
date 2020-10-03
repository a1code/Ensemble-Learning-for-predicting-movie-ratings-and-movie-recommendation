# Ensemble-Learning-for-predicting-movie-ratings-and-movie-recommendation

**Dataset** : [MovieLens ml-latest (Last updated 9/2018)](https://grouplens.org/datasets/movielens/)  

**Implementation summary** :  
- Explored collaborative filtering approaches to predict unknown user ratings on the MovieLens dataset.

- Implemented a neural network using Keras, and utility matrix decomposition algorithms like SVD, NMF, CoClustering and ALS using Pandas, Surprise library and Spark MLLib.

- Evaluated all models for accuracy in predicted ratings and top N recommendations, and built an ensemble to achieve improved RMSE and F-measure over all individual models except SVD.  

**Abstract** :  
Today we have the ability to collect data from user-item interactions on online platforms. Many such platforms aim to enhance customer engagement, loyalty and purchases by suggesting new items of interest to the user. This is crucial to maximize traffic and revenues for the organization. Content-based recommendations and collaborative filtering are well known approaches to recommend new items to users based on their known ratings of certain items. In practice, there can be many approaches to train a model which take user as input and predict ratings for items that are unrated by that user. New items can then be suggested to the user in the non-increasing order of predicted ratings. However, it is observed that the best results are obtained by combining results from multiple models, rather than using a single model.  
In this work, an ensemble learning technique is proposed that combines ratings predicted by multiple collaborative filtering models - trained with neural network, Singular Value Decomposition, Non-negative matrix factorization, CoClustering and Alternating Least Squares algorithms. Through this, the objective is to learn a predictor on the MovieLens ml-latest dataset. Such a predictor should be able to recommend movies to users based on predicted ratings such that the recommendations are as relevant, and prediction errors as minimized, as possible.  
Note: Exploratory Data Analysis is only done for a smaller sample of the full dataset (ml-latest-small), due to computing and time constraints.  

**Observations** :  
| Model          | MAE    | RMSE   | Precision | Recall | FMeasure |
|----------------|--------|--------|-----------|--------|----------|
| Neural Network | 1\.011 | 1\.307 | 0\.773    | 0\.773 | 0\.773   |
| SVD            | 0\.647 | 0\.848 | 0\.832    | 0\.832 | 0\.832   |
| NMF            | 0\.688 | 0\.902 | 0\.82     | 0\.82  | 0\.82    |
| CoClustering   | 0\.712 | 0\.92  | 0\.827    | 0\.827 | 0\.827   |
| ALS            | 1\.048 | 1\.339 | 0\.774    | 0\.774 | 0\.774   |
| Ensemble       | 0\.679 | 0\.876 | 0\.823    | 0\.823 | 0\.823   |
