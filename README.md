# Auto Insurance Loss Ratio Predictions
We will develop a predictive model that predicts loss ratio for each portfolio of auto insurance policies. The loss ratio is the ratio of total losses to the total premium of the amount. 
The key idea is to create a predictive model that gives an advantage for an auto insurance company to predict loss ratio of policies. This advantage will give an insurance company opportunity to make a decision of premium rates based on the overall risk of a portfolio.  The key problem is that 50% of all policies can be mispriced by more or less than 10%. 
The model will be built on a database of historical 400k input samples of auto insurance policies which have 69 features. Most of these features are categorical. The training dataset will comprise a set of attributes of portfolios, such as policy number, vehicle make year, vehicle usage, driver age, marriage status, annual premium, claim count, loss amount, loss ratio, and other attributes. The target will be natural logarithm of the loss ratio of portfolio. We also have a testing dataset of 330 testing portfolios. Each portfolio consists of 1000 to 5000 policies. The difference between training dataset and testing dataset is that testing dataset does not have loss amount, loss ratio, claim count, freq., and severity. The problem which we will face during this project is that our dataset is imbalanced, and we might have outliers.
The first step will be exploratory data analysis. During this step we need to get information of datatypes, for better understanding what attributes are numerical and what are categorical. We need to display a statistical overview of the data, and check if we have any missing data. Also, we will use pandas-profiling to get a report of our data. The report will give us a better understanding of our data. The correlation will help us to find a pairwise correlation of all numerical columns in the data frame. After that we can use the seaborn heatmap to get a better idea which variables are correlated. Moreover, since we already now that the majority of policies do not have a claim and we will face outliers, we will use donut pie chart to see what is the percentage of policies which do not have claims. And the last step of exploratory data analysis will be creating a histogram for the dataset to understand the distribution of numeric variables.
The next step will be data preprocessing. During this step we will need to select features, check missing values, and create dummy variables.  Then we will create portfolios of training data where each portfolio will have from 1000 to 5000 policies, and percentage of losses. For each training portfolio we will need to engineer a set of features that summarizes the data in that portfolio, for example, the mean of driver age.
After when we will create portfolios of the training data, we should choose what modeling techniques do we want to use to build the model: Regression, Decision Tree, Random Forest, Gradient Boosting algorithms such as XGBoost, kNN. Finally, we can use testing dataset to predict loss ratio.
For evaluation and computing the model performance we will use cross-validation which will allow us to get an estimated error over all the data. Then we will use confusion-matrix to check the model evaluation. 
