# Home-Credit-Default-Risk-Classification-Competition---Google-Kaggle

## Competition Backgroud
Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders. Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data--including telco and transactional information--to predict their clients' repayment abilities. While Home Credit is currently using various statistical and machine learning methods to make these predictions, they're challenging Kagglers to help them unlock the full potential of their data. Doing so will ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.


![dataset](https://github.com/WallaceSUI/Home-Credit-Default-Risk-Classification-Competition---Google-Kaggle/blob/main/competition-backgroud.png)

1. Home Credit company hopes to estimate customer loan default probability through data mining and machine learning techniques.

2. There are 7 tables with 218 initial features (335230 observations in training dataset and 48744 observations in testing dataset).

3. The final requirement of the game is to submit the default probability of each ID and the calculated AUC is used as the criterion.

## Our Methods and Results
1. After visualizing the initial data, we use Python to perform feature engineering processing on the original data set to create new features: 1): use the domain knowledge to perform basic operations, establish statistical information and deal with unconventional data and data missing values; 2): use features related to loan time and the number of loan as a node to process time series data; 3): based on different part of data, create the cluster analysis of data features and combine data individuals with their clustering groups to perform variance analysis. The 218 initial features are eventually increased to 4429 total features.

![dataset](https://github.com/WallaceSUI/Home-Credit-Default-Risk-Classification-Competition---Google-Kaggle/blob/main/feature-engineering.png)

2. We model the data using the machine learning and deep learning toolkits in Python: 1): use LightGBM, XGBoost, CatBoost and Neural Network (FFNN, CNN, RNN) to perform separate model training on the data; 2): use cross-validation method to divide the data into 5/7/10 subsets in order to test the training predictions; 3): use the bayesian optimization to adjust and optimize parameters for each model separately. In total, more than 100 different data model collocation schemes were combined, and 32 models were selected with relative higher accuracy for the next model fusion.

![dataset](https://github.com/WallaceSUI/Home-Credit-Default-Risk-Classification-Competition---Google-Kaggle/blob/main/modeling.png)

3. The Ensemble, Blending and Stacking algorithms are used to enhance fusion of each single model prediction result. The best result is combined with 4 LightGBM, 2 XGBoost, 1 CatBoost, 1 FFNN, 1 CNN and 1 RNN models.

![dataset](https://github.com/WallaceSUI/Home-Credit-Default-Risk-Classification-Competition---Google-Kaggle/blob/main/results-embedding.png)

4. A bronze medal at the end.
