# Prosper Loan Data Exploration

## Dataset

This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.

The dataset: https://www.google.com/url?q=https://www.google.com/url?q%3Dhttps://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv%26amp;sa%3DD%26amp;ust%3D1581581520570000&sa=D&source=editors&ust=1673956845335289&usg=AOvVaw3Wl4Ss_9yGMm5_q96laEhn

This data dictionary explains the variables in the data set. https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&source=editors&ust=1673956845335923&usg=AOvVaw1WIWAaVHyJiBwVBz12CR5B


## Summary of Findings

My initial exploration led the following findings:

The mean loan amount is around $9 000 and 55% of loans are below $9 000. Surprisingly the majority of loans are taken out to pay off existing loans, accounting for almost 70% of all loans in the dataset. Unfortunately no category descriptions are available for the two runner up categories i.e. not available and other. The fourth and fifth biggest categories are home improvement and business loans respectively. The prosper scores are mostly in a mid range between 4 and 8. The majority of borrowers earn in the income ranges of 25,000-49,999 and 50,000-74,999 USD income range. The bulk of borrowers are employed at least partially, if not full-time. It would appear that obtaining a loan as self-employed, retired or employedd part-time would be surprisingly difficult.  The majority of the loans in this dataset is either current or completed. The majority of borrowers don't have any delinquent trade history. Almost 70% of the loans are mid term i.e. 3 years. Borrowers have an average of 10.32 current credit lines. 

Positive and highly correlated observations for numerical data:
* Lender yield vs estimated effective yield
* Lender yield vs estimated loss
* Lender yield vs estimated return
* estimated effective yield vs estimated loss
* estimated effective yield vs estimated return
* estimated loss vs estimated return

For the rest of the analysis focused on estimated loss vs lender yield as main variables of interest.

A positive correlation is observed between with estimates loss and lender yield. The higher the lender yield the higher the estimated loss. Various factors could increase lender yield such as higher interest rates, which are usually implemented when the loan involves risk factors. There is a positive correlation observed between loan amount and the number of current credit lines among borrowers. There is a negative correlation between loan amount and lender yield.

Key differences between borrowers with an employment status of employed versus full time is observed. The trend of the majority of employed borrowers follow fixed curves in the estimated loss vs lender yield space, however full time employees do not follow these trends and have a much larger spread in lender yield for a given estimated loss.

The lower the prosper score the higher the estimated loss. Although the same is observed for the lender yield and prosper score relationship, the lender yield varies immensely for given estimated losses. Some factors such as borrower interest rate, delinquent payments, debt to income ratio and income range may potentially increase or decrease lender yield. 

Differences were observed in the lender yield for the three different loan terms. 12 month loans have a lower lender yield, but similar estimated losses compared to 36 month and 60 month loans. 60 month loans have the highest lender yield. We also find that lender yields around 0.3 for the 36 month term have a large range of estimated losses where estimated losses significantly increase.


## Key Insights for Presentation

For the presentation, I focus on relationship between estimated loss and lender yield and leave out most of the intermediate derivations. I start by introducing the relationship between the estimated loss and lender yield as a bivariate plot.

The categorical variables are introducd to the bivariate plot to produce multivariate observations. This shows where they are distrubuted with respect to the estimated loss and lender yield plot. Some interesting patterns are observed with the use of colour. The categorical variables introduced include: Employment status, loan term and prosper score.
