
## Loan Data from Prosper Data Analysis and Visulization


## Table of Contents
- [Introduction](#intro)
- [Part I - Data Wrangling](#wrangle)
- [Part II - Exploratory Data Analysis](#analysis)
- [Part III - Conclusion](#conclusion)

<a id='intro'></a>
### Introduction
The dataset that we are interested is the dataset of 'Loan Data from Prosper', which contains information about the listing, borrower, propser, and loan. **We will maily focuse on the borrower's side in this project. **

A detailed introduction about the data set could be found at: https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0 

After data wrangling and cleaning, we firstly looked into the borrower's state (location) and occupation, and their relationships with stated income. We also checked the relationship between the borrower's Annual Percentage Rate (APR) and interest rate for the loan. Lastly, we investigated the possible relationship among BorrowerRate, CreditScoreMean, AmountDelinquent, and StatedMonthlyIncome. A negative correlation between BorrowerRate and CreditScoreMean was found, which were further verified on groups of borrowers with different occupation. 


<a id='wrangle'></a>
### Part I - Data Wrangling

In this section of the report, we loaded and trimed the dataset, and then assessed and cleaned it for further analysis. **A detailed wrangling process could be found in'exploration_template.ipynb'.**The major changes are list below:

`1.` Since we are focused on the borrower's side, we only kept the columns of ListingNumber, LoanStatus, BorrowerAPR, BorrowerRate, BorrowerState, Occupation, EmploymentStatus, CreditScoreRangeLower, CreditScoreRangeUpper, CurrentCreditLines, OpenRevolvingAccounts, CurrentDelinquencies, AmountDelinquent, DelinquenciesLast7Years, IncomeRange, IncomeVerifiable, StatedMonthlyIncome.

`2.` The dataframe looks quite clear, we mainly solved the problems of missing data and replication by removing the repetead rows and rows with missing value. There are out of 113937 samples remained.

`3.` We created a new column named as CreditScoreMean, which is calculted as the mean of CreditScoreRangeLower and CreditScoreRangeUpper. This data could be used as the credit score for borrowers.


<a id='analysis'></a>
### Part II - Exploratory Data Analysis

We explore possible relationships in the data set by univariate, bivariate, and multivariate plots. **Please refer to slide_deck_template.slides.html' or 'slide_deck_template.ipynb' file for detailed explanatory analysis and conclusion. ** 

<a id='conclusion'></a>
### Part III - Conclusion

Please refer to 'exploration_template.ipynb', or 'slide_deck_template.slides.html'.We mainly answered the following questions:

**Where do the borrowers come from? What do they do?How much do they earn monthly?**

**How's the stated income distributed for borrowers from different state/occupation?**

**Any relationship among BorrowerRate, CreditScoreMean, AmountDelinquent, and StatedMonthlyIncome?**

