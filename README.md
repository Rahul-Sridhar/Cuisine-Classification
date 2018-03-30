# Cuisine Classification from Ingredients

### **Description:** The main purpose of this project is to classify cuisines based on Ingredients of the Reciepe.


The steps followed are as follows:
* Step-1: Download dataset from [https://www.kaggle.com/c/whats-cooking/data](https://www.kaggle.com/c/whats-cooking/data), store it in dictionary and convert it to dataframe.
* Step-2: Feature Selection:
  * Removal of punctuation, digits, content inside parenthesis using Regex Expression
  * Remove brand names using Regex Expression
  * Convert to lower case and Remove stop words using Regex Expression
  * Use Porter Stemmer Algorithm
* Step-3: Encoded Cuisine column using Label Encoder of sklearn.
* Step-4: Convert the ingredients column after feature selection into TFIDF Matrix
* Step-5: Split the data(X-TFIDF Matrix, Y-Label Encoded value of Cuisine into training and test data(80:20).
* Step-6: Use Different Machine Learning Algorithm to get best accuracy. 


# Conclusion
The OVA SVM Algorithm gives the best accuracy of 78.88% for the given dataset.

|       Algorithm       |           Parameters           | Accuracy |
|:----------------------|:------------------------------:|:--------:|
|          KNN          |              K=25              |  74.81%  |
|        OVA SVM        |              C=1               |  78.88%  |
|      Crammer SVM      |C=1, multi_class=crammer_singer |  78.84%  |
|    OVA Naive Bayes    |               -                |  66.71%  |
|OVA Logistic Regression|               -                |  77.72%  |
