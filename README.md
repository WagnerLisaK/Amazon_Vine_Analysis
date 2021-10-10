# Amazon Vine Analysis

## Overview
This project analyzed Amazon reviews written by members of the paid Amazon Vine program.  This program is a service that allows manufacturers and pulishers to receive reviews for their products.  Some companies pay a small fee to Amazon, provide their product to the Amazon Vine members, who are then required to submit a review.  I chose to analyze reviews for Major Appliances.

## Results
The questions posed are as follows:
  * How many Vine (paid) reviews and how many non-Vine (unpaid) reviews were there in total?
  * How many Vine (paid) reviews and how many non-Vine (unpaid) reviews were 5-star?
  * What percentage of Vine (paid) and non-Vine (unpaid) reviews were 5-star?

Below is a snippet of the full dataset:

![Full_dataset.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Full_dataset.png)

The following steps were taken to find the results of the above questions:
  1. The review id's with less than 20 total votes were removed from the dataset.
        * The data is skewed to the right, but reduces the overall skewness (28.3) down to 9.4 by removing the reviews with less than 20 total votes.
        
        ![Votes20_DF.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Votes20_DF.png)
        
        ![skewness_total_pop.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/skewness_total_pop.png)   ![skewness_20votes.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/skewness_20votes.png)
               
  2. The review id's that contained less than 50% of "helpful" votes were then removed, further reducing the skewness to 9.1.
        * This still means the data is skewed right to a major degree.
        
        ![Helpful_Votes.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Helpful_Votes.png)
        
        ![skewness_50pct.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/skewness_50pct.png)
        
  3. The dataset was then separated into 2 subsets: Vine (paid) reviews and non-Vine (unpaid) reviews.
        ![Paid.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Paid.png)
        
        ![Unpaid.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Unpaid.png)
  
  4. The percent of 5-star reviews was then calculated per each dataset.

Below are the results:

![Results_no_code.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Results_no_code.png)


## Summary

Is there any positivity bias within the Vine (paid) program??  What other analysis could support my findings.

## Reference

Below are the additional code blocks used to perform this analyses:
![Major_Appliances.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Major_Appliances.png)
![Final_Code1.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Final_Code1.png)
![Final_Code2.png](https://github.com/WagnerLisaK/Amazon_Vine_Analysis/blob/main/Resources/Final_Code2.png)

Submitted by Lisa K Wagner (10/10/2021)
