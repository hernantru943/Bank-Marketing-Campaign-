# Bank Marketing Campaign Prediction
 Hernan Trujillo

### Abstract

The purpose of this project is to help bank institutions to determine if a client will subscribe to a Term Deposit. In order to achieve this, I built a model to predict how effective is the marketing campaign with phone calls to current clients based on their atributes. If the bank is able to apply an effective model to increase Term Deposit subscribers, they will make a significant profit. There are many variables and features associated with subscribers, which can be use to build the model. 

### Design

The question of whether a client will subscribe or not can be solved by using supervised learning as a classification tool. Doing a hard prediction will help me predict whether the client will subscribe or not to a Term Deposit. The lending institution is trying to expand the number of clients subscribed to Term Deposits as a business oportunity.

### Data

Dataset of 20 features in total with 50% numerical and 50% categorical. Also 41k observations or clients contacted.

### Methodology

### Data Collection and Manipulation

Gathered data from UCI Machine Learning Repository https://archive.ics.uci.edu/ml/datasets/Bank+Marketing and did  enough feature engineering to make sure my data was in a good shape to be modeled.

### Modeling

- Logistic regression
- Logistic Regression (Handling Class Imbalance)
- Naive Bayes
- Random Forest

Logistic Regression (Handling Class Imbalance) got a F1 score of 0.39 

class_weight = "balance" to make it equal ratio


The class imbalance for original dataset is 89% (negative) vs 11%(positive)

### Tools

- Tableau https://public.tableau.com/app/profile/hernan.trujillo/viz/BankMarketing_16274215803320/Dashboard1
- Pandas
- Numpy
- Sklearn
- LogisticRegression
- RandomForestClassifier
- Confusion_matrix
- Classification_report
- Matplotlib 
- Seaborn

### Communication

In terms of the categorical features (50% of the total features) importance, I found out the following observations:

- Job: The top three professions that our customers belong to are - administration, blue-collar and technician jobs. 25% comes from admin jobs.
- Marital: A huge number of the customers are married (60%).
- Education: Client with university degree (29%) and high school (23%) were approached more as compare to other and they have higher success rate as well. (in terms of term deposit number).
- Default: Majority of the customers do not have a credit in default (82%). This variable has no impact on the client subscribing for term deposit. As we can see with no as input client took the term deposit and client having credit are not taking term deposit. So we will drop this feature.
- Loan: We approach around 84% of client with not having personal loan. Only a few have applied for it (16%).
- Housing: Housing loan doesn't seem a priority to check for since an equal number of customers who have and have not subscribed to it seem to have subscribed to the term deposit.(Yes:54%, No:46%)
- Contact: Cell-phones seem to be the most favoured method of reaching out to customers (63%).
- Response(Target):The target variable shows heavy imbalance (No= 89% / Yes= 11%).
- Month: Many customers have been contacted in the month of May (33%).
- Day of week: We have 5 days collected values. There is no significant different in the number of client approached and number of people subscribed.
- Poutcome: If a client took the term deposit last time then there is higher chances of that client subscribing to it again.

Also, one of the crucial feature engineering work I did was transforming categorical data into numerical for modeling purposes.

![Final Score F1 Models](https://user-images.githubusercontent.com/77758249/128502107-677bbf8f-155b-46f1-b696-49a344877c8e.png)

