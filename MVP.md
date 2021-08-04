## Bank Marketing Campaign Prediction
#### How many clients will subscribe to a term deposit investment account during a marketing campaign?

Preliminar data exploration using Tableau and Python indicates the following: https://public.tableau.com/app/profile/hernan.trujillo/viz/BankMarketing_16274215803320/TotalOutcome#2

Observations of categorical variables:

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

![correlation_heatmap](https://user-images.githubusercontent.com/77758249/128150358-2db2aef3-18f1-48de-b153-f04fee0ee469.png)

Also, there are no features that are highly correlated and inversely correlated. If we had, we could have written the condition that if the correlation is higher than 0.8 (or can be any threshold value depending on the domain knowledge) and less than -0.8, we could have drop those features. Because those correlated features would have been doing the same job.

![confussion_matrix](https://user-images.githubusercontent.com/77758249/128150833-5526f1c6-faee-4854-9b1b-b41465d4b4ff.png)

#### Preliminar results on the basic Logistic Regression Model:

Accuracy for Logistic Regression model is: 0.9047120418848168
F1_score for Logistic Regression model is: 0.272

Confusion matrix 
 [[3388   40]
 [ 324   68]]

AUC Score 0.7599326821075418
roc_auc_score 0.5842295963106987

Scoring on Training Data: 0.8982695942998401
Scoring on Test Data: 0.9047120418848168

#### Notes on Results:

- Accuracy in score is good
- F1 Score is too low
- Model score on Training and Test dataset is good which tell us no Overfitting/Undersitting of the model
- AUC score is good
- Confusion matrix shows values for TN, TP, FP and FN. Our aim is to get the lower False Positive which is pretty good in this model
