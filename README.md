Credit Card Fraud Detection using Logistic Regression

- Project - Credit Card Fraud Detection
- Skills - Logistic regression , Support Vector Machine, K Nearest Neighbours, F1 Score, ROC-AUC Curve, Data Visualisation , Exploratory Data Analysis , Data Science application in Finance , Machine Learning
- Tools - Google Colab , Jupyter Notebooks , Python , Numpy , Pandas , Matplotlib , Seaborn , Sklearn

  ## The Dataset:
  The data was taken from Kaggle site :  https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud .

  The Columns do not have physical significance directly visible since as per the source (Kaggle) , the data was compressed using Principle Component Analysis (PCA) in order to protect the privacy of the individuals while making a realistic secnario dataset availaible to public .

  ## Data Preprocessing and Visualisation:
  ![Screenshot 2025-05-31 230253](https://github.com/user-attachments/assets/488c9998-1197-471f-b428-ff1a5b9ccd8e)
## CORRELATIONS
![Screenshot 2025-05-31 230640](https://github.com/user-attachments/assets/e8b3db47-f36c-4bb1-accb-73df8399ae68)
## Class Imbalance in dataset:
![Screenshot 2025-06-01 001542](https://github.com/user-attachments/assets/37b4342e-0b16-4575-b201-ed59c3ccc9cd)
This shows that we have way way less data for fraud cases than for non fraud cases , which is expected from the dataset .

To cure imbalance , we can use undersampling or oversampling . Here , I have decided to use SMOTE to counter the class imbalance in the dataset .
## Result from part 1:
![Screenshot 2025-06-01 001806](https://github.com/user-attachments/assets/62c90e08-be1a-47da-abb0-5f0df3bb350c)
The F1 score came 0.99 meaning the Classifier is working great . It managed to catch 91 out of 101 frauds , thus preventing frauds 90% of the time . The confusion matrix , precision , recall and F1 score has been displayed for your convenience . The confusion matrix readings and the F1 show the success of the project .
## Result from part 2:
I have also uploaded some raw code to this repository , here are the conclusions derived from it :
Frauds are time independent so we can drop time :
![Screenshot 2025-06-01 002144](https://github.com/user-attachments/assets/9c80e684-8536-4227-a831-f319c8d11e2c)
**Lower Dimension Visualization** is beautiful:
![Screenshot 2025-06-01 002307](https://github.com/user-attachments/assets/5e9c4133-24f0-4aab-9bf5-683a9282cd4c)
I also took advice from my seniors, decided to undersample the dataset since significance of the data would be more realistic if there was no synthetic dataset. I also decided to choose the ML model with most recall , reason being that I realized later that as a business, labelling a Non Fraud datapoint as fraudulent would be much more worse for the company, since nobody would like their card to decline and people would literally stop using that credit card, so we must focus more on achieving lower recall than only blindly improving F1 score . So I got Logistic regression as the winner again with the following results :
![Screenshot 2025-06-01 002542](https://github.com/user-attachments/assets/a0d75b26-39f5-4575-9ab1-2603d024e27b)
