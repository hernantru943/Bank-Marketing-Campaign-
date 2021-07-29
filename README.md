# Bank Marketing Campaign
Building a classification model to predict if a client will subscribe a term deposit investment account

#### Question/need:

* What is the framing question of your analysis, or the purpose of the model/system you plan to build? 

Based on a Bank marketing phone calls gathered from direct marketing campaigns, I will build a classification model to predict how many clients will subscribe a term deposit investments account. 

* Who benefits from exploring this question of building this model/system?

Banks and Credit Unions are businesses, as such, they want to increase the number of Term Deposit Investment Accounts within their current clients or new ones. When an account holder deposits funds at a bank, the bank can use that money to lend to other consumers or businesses, as well as investing in other sectors such as real state as an example. This practice increases their margins or profitability so having a model that can predict the effectiveness of their marketing campaigns by  targeting the potential clients for term deposit accounts becomes a smart business decision, when they can use the data to leverage the business by applying Data Science. 

#### Data Description:

* What dataset(s) do you plan to use, and how will you obtain the data?

I am planning to use a data set from UCI Machine LEarning Repository that contains 41,188 observations and 20 features besides the target column called "y".
source: https://archive.ics.uci.edu/ml/datasets/Bank+Marketing

* What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with? 

I have plenty of useful features in my dataset, but I'd mention as some of the most relevants as the Campaign: number of contacts performed during this campaign and for this client, Duration: last contact duration, in seconds, Marital : marital status and Loan: if the client has personal loan, among others.  

* If modeling, what will you predict as your target?

y: has the client subscribed a term deposit? (binary: 'yes', 'no')

#### Tools:
* How do you intend to meet the tools requirement of the project? 

I am going to perform an initial EDA Pandas for processing, visualization, and production. Then, I am going to build a Classification Model by using python package sklearn.

* Are you planning in advance to need or use additional tools beyond those required?

I will also use Tableau for visualization purposes since is an effective tool for communicating results and analysis.

#### MVP Goal:
* What would a [minimum viable product (MVP)](./mvp.md) look like for this project?

A minimum MVP will consist on plotting some data for visualization analysis with Tableau by comparing the target (users subscribeb to a term deposit - yes/no)with features such as age, marital status, education, last contact call duration, last contact day and month. The initial purpose of this analysis is to understant the relationships between them with the target and how they impact the results. Then we can consider this results when selecting our features to build our model.

Here is a Tableau link with this preliminar visualization: https://public.tableau.com/app/profile/hernan.trujillo/viz/BankMarketing_16274215803320/LastContactbyMonth#1
