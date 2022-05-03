# Is There a Correlation Between the Incidents of Fraud vs. The Spending Size, Population Size, Age Group and Demographics?

# Project Overview 
Credit card fraud transactions are a fear that many americans have as they happen so frequently! They cost financial companies and conusmers themselves millions of dollars every year. Is there a better, more efficent way to detect whether a transaction is fraudulent or not in real time. If so, which parameter is it? 

By looking at a dataset with over 550,000 transactions, and analyzing the other identifying factors that were in those transactions, we aim to discover any actionable insights.

# Project Structure
For this project, we used a dataset with different parameters and tried to find which one was most efficent.

Our final code can be found in mjrafol/EDA_Project-1.

Finally, we created a powerpoint slide to summerize our findings and insights.

# Project Contributors
- Taib Diallo
- Alexis Hernandez
- Yuanfeng Xu
- Mary Jane Rafol
 # Objective
Analyze the fraud data set to determine correlation between fraud incidence, spending size, age group, demographics and time of transaction so awareness campaigns can be directed to these groups. Perform other relevant analysis from the data set.

Statement: There is no correlation between the spending size, age group, demographics and time of transaction vs. fraud incidence.

# Hypothesis
Ha = There is strong positive correlation between the spending size, age group, demographics and time of transaction and fraud incidence.

Hb = There is strong negative correlation between the spending spending size, age group, demographics and time of transaction and fraud incidence.

Ho = There is no correlation between the spending size, age group, demographics and time of transaction and fraud incidence.
# Methodology
We identified Kaggle’s Simulated Credit Card Fraud Dataset, used the pandas Application of Pandas’ cut / bin and groupby functions on Dataset, and requested Census API to do bar chart, scatter plot and and linear regression.
![image](https://user-images.githubusercontent.com/100816322/166395383-5d119dac-8b42-4f4c-a4b1-5b59fbd53efe.png)
# Results #1:  Spending Size
Our analysis shows no strong correlation between users average spending and its susceptibility to fraud.  
The r-value returns to 0.28, which is closer to 0, suggesting weak correlation between the two variables!

![image](https://user-images.githubusercontent.com/100816322/166395518-bc1de780-d05f-4264-a00a-c9c58e96487a.png)
# Results #2: Age Group
Our analysis shows that the rate of fraud incidents are higher on credit card users 58-100 yrs. old (Boomers, Post-War and WWII).  
This result also supports the premise that older people have wealthier financial status, and they tend to be more trusting and forgetful, increasing their vulnerability therefore they become high susceptible targets. 
![image](https://user-images.githubusercontent.com/100816322/166395634-5fce53fc-b6a5-4686-ade4-4814bc3a746d.png)
# Results #3: Demographics

1. Heatmap for distribution of victims' location
![image](https://user-images.githubusercontent.com/100816322/166395787-05b07399-489e-4b65-995a-2f691ad51dc2.png)

2.Based on the previous statistics data for 2020:"Population sizes play a large role in which states have the most identity theft credit card fraud." https://www.fool.com/the-ascent/research/identity-theft-credit-card-fraud-statistics/. California has the highest number of identity theft incidences (of which credit card fraud is the most typical), and Georgia has the most cases per capita, according to a 2019 Federal Trade Commission report.

Hypothesis 1. Big cities that have larger population size tend to have higher fraud incidences.

Based on the analysis of our dataset,the r value is 0.06900267483096204 and the r-squared is :0.00476136913382749. The correlation between city population size and credit card fraud incidents is weak. The hypothesis1 is rejected.
![image](https://user-images.githubusercontent.com/100816322/166395971-b21a13b5-5e89-44d1-bd76-55c59198cd44.png)

3.Census API:
Get the data about population data and other economic data for all states in 2020 and combine our state sub-dataset and census dataset.
![image](https://user-images.githubusercontent.com/100816322/166396047-0a2f0515-93fc-44d5-b08c-8864c0064699.png)

4.Hypothesis 2. States that have larger population size tend to have higher credit card fraud incident rate.

The r value 0.59 indicates that state population size  is positively correlated with the rate of fraud incidences.
The r-squared shows that the rate of fraud incidence can be explained 35% of the variance by the state population in the regression model.
The Hypothesis 2 is accepted.
![image](https://user-images.githubusercontent.com/100816322/166396154-01050a99-2a40-40ea-919d-186358d057bf.png)

5.Hypothesis 3. Socioeconomic status (measured by poverty rate, unemployment rate, household income, per capita income) is correlated with credit card fraud incident rate. (Base on previous research about the correlation between socioeconomic status and criminal behavious, we put forward this hypothesis.)

Hypothesis 3a Poverty rate is positively correlated with credit card fraud incidents rate.

Hypothesis 3b Unemployment rate is positively correlated with credit card fraud incidents rate.

Hypothesis 3c Household income is negatively correlated with credit card fraud incidents rate.

Hypothesis 3d Per capita income is negatively correlated with credit card fraud incidents rate.

Base on our regression models, the correlation between socioeconomic status and credit card fraud rate is weak. The r-squared shows that the regression model  can not explain the relationship. The Hypothesis 3  is rejected.
![image](https://user-images.githubusercontent.com/100816322/166396304-d9ce3db3-24d9-4224-9786-0e282038b336.png)

The correlation coefficient between poverty rate and fraud incidents is (0.15441884405064088, 0.31114870168065645)
The r-squared is :0.023845179397936147

![image](https://user-images.githubusercontent.com/100816322/166396364-60f0a339-f594-49e7-85e3-cfe941da4eab.png)

The correlation coefficient between unemployment rate and fraud is (0.06465200169484829, 0.6730714556206687)
The r-squared is :0.004179881323150668

![image](https://user-images.githubusercontent.com/100816322/166396395-537a6842-cf1f-4449-9dfe-27716b04fa33.png)

The correlation coefficient between Household Income and fraud incidences is (-0.11243119350502423, 0.46214218157102943)
The r-squared is :0.012640773272964206

![image](https://user-images.githubusercontent.com/100816322/166396504-7c626c30-f9a7-440d-8eb9-bcfcaf0d61be.png)

The correlation coefficient between Per Capita Income and fraud is (-0.07854832687251433, 0.608032298861484)
The r-squared is :0.006169839654471365

# Results #4: Time Frame
Hypothesis 4. Night-time and early morning have more credit card incidence rate. (Base on the previous statistics data, the identity theft usually happened in the early morning. Therefore, we put forward this hypothesis.)

Based on the analysis, the top three time that has high-frequency of fraudulent transactions: 22 o’clock,, 23 o’clock and 3 o’clock.

Night-time and early morning time tend to have higher credit card fraud incidents rate.
Hypothesis 4 is accepted.

![image](https://user-images.githubusercontent.com/100816322/166397102-b34dfeae-51fc-4a5c-953a-171753f710be.png)
![image](https://user-images.githubusercontent.com/100816322/166397110-2cc74ebb-24ee-4a5c-ad87-7ccfee7d0957.png)

# Other Analysis
1. Purchase Categories vs. Fraud Incidence 
  Top categories :Online, POS-Grocery and POS-Shopping
![image](https://user-images.githubusercontent.com/100816322/166397382-ee76758d-dcfd-4a9a-ae77-3c3c608a9e75.png)

2. Max fraud commit per category
Average amount of fraud for all transactions reported during the period was $528.More than a third of all fraud reported during the period were related to online activities.Online scammers do not discriminate age, is the top category for all age ranges.Amount average per online fraud reported is $928. 
During the period studied, the top three categories exceeded one million dollars in fraud. Frauds credit card not present reach 63% of the total.
![image](https://user-images.githubusercontent.com/100816322/166397494-3d9a16e9-38db-41f5-9906-f66d7657b76c.png)

3. fraud vs. distance
The distance between victims' locations and fraudulent transactions' locations was calculated. The maxmum, minimum, mean and median distance was found. The bar chart showed the relationship between mean, median, max and minimum distance between fraudulent and nonfraudulent transactions.
![image](https://user-images.githubusercontent.com/100816322/166398733-8940e0a5-b8ad-41a2-9b39-7fa7460658af.png)
![image](https://user-images.githubusercontent.com/100816322/166398777-49e3c98d-d06e-4d89-9c23-2b5bb3d8795f.png)

# Conclusion
There is no correlation between the victim's average spending size and fraud incidence. This result does make sense whereby fraudsters are usually unaware of the credit card users spending activity. The user's spending activity is not a public information available.

Our analysis showed that the incidence rate for age groups 58-100 yrs. old (Boomers, Post-War and WWII) are higher making them more susceptible victims of credit card fraud. In a general sense, users at this age tend to be more trusting and forgetful, making them more vulnerable.

The is a strong correlation between state population size and fraud incidence. States with higher population tend to have higher credit card fraud incident rates. Our analysis also showed weak correlation on victim's socio economic status (poverty rate, unemployment rate, household income, per capita income) and fraud incidences.
Night-time and early morning time tend to have higher credit card fraud incidences rate.

# Limitation
The dataset is limited to seven months only and does not provide historical data to enable trending per year.

The credit card records do not seem to be distributed reasonably across, cities, age group—analysis could have improved if these limitations are addressed. 

The dataset is limited to 45 states and 52 cities

# Future Exporatory Analysis

1. Future analysis can explore the relationship between credit card fraud incidence and Gender
Job type and Merchant categories.

2.Develop a code that flags suspicious incidences once transaction meets the following requirements: age of the victim, location of the transaction, amount, card holder's home address, merchant category, etc.

# References
https://www.kaggle.com/datasets/kartik2112/fraud-detection

https://www.fool.com/the-ascent/research/identity-theft-credit-card-fraud-statistics/

https://www.cardrates.com/advice/credit-card-fraud-statistics/

https://www.experian.com/blogs/ask-experian/dont-let-id-thieves-ruin-your-birthday-or-any-other-day/

https://en.wikipedia.org/wiki/Statistical_correlations_of_criminal_behaviour
