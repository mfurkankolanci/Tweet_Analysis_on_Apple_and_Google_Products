
# Apple Advertising on Twitter


###  Overview
Project four for Flatiron Data Science BootCamp. In this Project we used various classification algorithms to accurately identify sentiment of tweets towards Apple and Google products. We start by importing neccassary packages, cleaning/text preprocessing the data and building our baseline model. We want to be able to accurately classify neutral and negative sentiments in order to help our stakeholders target ads towards the correct twitter users. Some of our recomendations include also sending apple product advertisements toward twitter user's who had unplesant experiences with Google in order to gain new customers.


### Stakeholder
Apple's advertising team

### Business Problem
Apple's advertising team has noticed that some Twitter users have not had positive experiences with Apple products. In order to not lose those customers, they would like to have targeted ads towards those users. Our stakeholder is also interested in tweets about Google and they would like to turn this into their advantage by converting these users into Apple customers. Therefore, they have asked our team to generate a model that performs sentiment analysis in order to categorize tweets about Apple and Google as positive, neutral and negative, so that the stakeholder knowns which users to target with their ads.


### Data
Our Dataset was imported from https://data.world/crowdflower/brands-and-product-emotions.
The dataset is from the year 2013 and includes more 9,000 tweets. There are three columns, the first column includes the tweet text, the second column is the subject of the tweet and third column is the emotion of the tweet.

### Methods
For our methods we first prepared the data , then we grouped all the products under two labels, Apple and Google. This was done as Apple and Google products were scattered in the dataset and had to be regrouped. Then, we used regex to get rid of unimportant characters in the tweets. After that, we tokenize the tweets to split each tweets into its respective words so that each word is a feature in the model. We also remove stopwords as they provide little to no sentiment value to the tweets. Lemmatization is performed to group words with the same meaning together as one word. TF-IDF is applied in order to assign each word in each tweet a numeric value based on its importance across all tweets. Finally, random oversampling is applied in order to eliminate the class imbalance observed in the target variable (sentiment). We used pandas to perform data filtering and visualization, nltk to perform text preprocessing, imblearn for oversampling and sklearn for TF-IDF. For modeling, we utilized the sklearn's LogisticRegression, DecisionTree and RandomForestClassifier methods. We tuned our models using GridSearchCV also provided by sklearn.

### Conclusion 
The goal of this project was to come up with a method to perform sentiment analysis on tweets about Apple and Google products.In order to do so, we have created multiple classification models and identified the best one as a random forest model with an accuracy of 63%. This model will allow our stakeholder to identify the priority (negative and neutral) users and target their ads accordingly.

### For More Information
Please review our full analysis in our Jupyter Notebook or our presentation.

### Repository Structure
Describe the structure of your repository and its contents, for example:

├── README.md <- The top-level README for reviewers of this project, you are reading it right now.

├── https://docs.google.com/presentation/d/1Wy7Z5mpkqTLzUsuMDgLRJNFMJk_4zjdAgajiyG8qK5c/edit#slide=id.gfb44c67d90_1_3548 <- PDF version of project presentation

├── code

│ ├── init.py <- .py file that signals to python these folders contain packages

│ └── ipynb_checkpoints.ipynb <- Notebook containing a project checkpoint

├── Dataset <- Both sourced externally and generated from code

└── images <- Both sourced externally and generated from code