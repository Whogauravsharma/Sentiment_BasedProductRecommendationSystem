# Sentiment Based Product Recommendation

## Problem Statement

The e-commerce business is quite popular today. Here, you do not need to take orders by going to each customer. A company launches its website to sell the items to the end consumer, and customers can order the products that they require from the same website. Famous examples of such e-commerce companies are Amazon, Flipkart, Myntra, Paytm and Snapdeal.

Suppose you are working as a Machine Learning Engineer in an e-commerce company named 'Ebuss'. Ebuss has captured a huge market share in many fields, and it sells the products in various categories such as household essentials, books, personal care products, medicines, cosmetic items, beauty products, electrical appliances, kitchen and dining products and health care products.

With the advancement in technology, it is imperative for Ebuss to grow quickly in the e-commerce market to become a major leader in the market because it has to compete with the likes of Amazon, Flipkart, etc., which are already market leaders.


## Solution Approach

* The dataset and attribute description can be found in the dataset\ folder.

* The dataset undergoes data cleaning, visualization, and text preprocessing using NLP techniques. The textual data (review_title + review_text) is vectorized using TF-IDF Vectorizer, which measures the importance of words relative to other documents.

* The dataset suffers from a class imbalance issue, and SMOTE oversampling technique is applied to address this problem before applying the machine learning models.

* Several machine learning classification models, including Logistic Regression, Naive Bayes, and Tree Algorithms (Decision Tree, Random Forest, XGBoost), are applied on the vectorized data and the target column (user_sentiment). The objective is to classify the sentiment as positive (1) or negative (0). The best model is selected based on various evaluation metrics such as accuracy, precision, recall, F1 score, and AUC. XGBoost is chosen as the better model based on these metrics.

* Collaborative filtering recommender systems are created using user-user and item-item approaches. The RMSE evaluation metric is used to evaluate the performance of the recommender systems.

* The code for sentiment classification and recommender systems can be found in the Sentiment_BasedProductRecommendationSystem.ipynb Jupyter notebook.

* The top 20 products are filtered using the improved recommender system. For each product, the user sentiment is predicted for all the reviews, and the top 5 products with higher positive user sentiment are selected. This functionality is implemented in the model.py file.

* The machine learning models are saved in pickle files under the pickle\ directory. The Flask API in app.py is used to interface with and test the machine learning models. The user interface is set up using Bootstrap and Flask Jinja templates in templates\index.html. No additional custom styles are used.

* The end-to-end app is done.


