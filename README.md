# Amazon_Vine_Analysis

## Overview

This module provided students the importance of Big Data and how it is able to provide information from millions of rows of data (petabytes).  This particular challenge
asks students to pull reviews from an Amazon data set for products sold in a particular category.  I chose health and personal care products. 

The Amazon data set contains reviews writen by members of a paid Amazon Vine Program as well as non-members of this program.  Companies paya small fee to
Amazon.  Reviewers of the companies' products are required to publish a review on the Amazon site.

Since there are millions of reviews for each dataset, students use Amazon Web Services (AWS) and PySpark to process data as personal computers and servers do not have enough processing power.  We use PySpark dataframes to perform
group bys and filters to be able to provide some insight into the reviews submitted by customers and Vine members.  We also explore RDS (remote data services) in Amazon Web Services
to provide another way to analyze data.

## Results

Big Data processing with over millions of rows takes more time.  AWS provides the power of multiple servers as well as data availability.  The Health and Personal Care data set had 5331449 rows.
After dropping NaN records, there were 5330701 rows.  Then,we contined to filter out any products that had less than 20 reviews and had 50% helpful votes. This ensured that we had a good population of reviews so that
the review wasn't skewed and based on a small number of reviewers.  So, we begin our analysis with 121322 reviews.  That's quite a drop from over 5 million.

    How many Vine reviews 497   and non-Vine reviews 120825  were there?	
	[ReviewCounts](https://github.com/gaudiom4git/Amazon_Vine_Analysis/blob/main/Images/VineMemberCounts.png)
	
    How many Vine reviews were 5 stars? 220 	How many non-Vine reviews were 5 stars?    74445   
	[5 Star Reviews](https://github.com/gaudiom4git/Amazon_Vine_Analysis/blob/main/Images/Vine5Stars.png)
	
    What percentage of Vine reviews were 5 stars? 44.27%    
	What percentage of non-Vine reviews were 5 stars?  61.61%

## Summary

Based on the results presented from the Health and Personal Care Vine program, we can determine that there is more of a positivity bias for non-paid Vine members.  Seems that Vine members are more critical of the products in this category as there is a higher 
percentage of 5 star ratings for the non-paid Vine members at 61.61% versus the Vine member 5 star reviews at 44.27%.

You can also group by the star ratings to see how many were 4 stars and above versus 2 or less stars.  A positive review can be considered a 4 or 5 star, 3 is neutral, and 2 or 1 is a 
negative bias.  Personally, the product would have to be outstanding for me to give 5.  So, there could be more positive reviews with 4 stars that should hopefully support the same 
findings as the 5 star.

Vine members 		4 or 5 star percentage is 350/497 or 70.42%					1 or 2 is 70/497  14%
Non-Vine members 	4 or 5 star percentage is 87462/120825 or 72.39%			1 or 2 is 26413/120825 21.86%

[Star Groupings](https://github.com/gaudiom4git/Amazon_Vine_Analysis/blob/main/Images/Vine4or5%20and%201or2%20Stars.png

So, including the other stars further proves more positivity for non-paid Vine members.   Although, there seems to be alot of neutral (3) for Vine members than non-Vine members.


