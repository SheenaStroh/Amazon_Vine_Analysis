# Amazon Vine Analysis

## Overview
Amazon has a program known as Amazon Vine where companies pay a small fee and provide products to members in exchange for those members writing a review of the product. In this analysis I took a selection of Electronics reviews and analyzed them to determine if the paid vine reviews had a positive bias compared to the unpaid reviews.

## Results
After loading all of the reviews into a PySpark notebook I was able to filter the reviews down to only the vine reviews using the following code:
![Vine_DataFrame](https://user-images.githubusercontent.com/85318060/137236097-cfbd8a0b-d0f7-4e59-85d8-d6d302adabf2.png)
Similarly, I was able to filter another DataFrame down to just the reviews that were not vine using the following code:
![Not_Vine_DataFrame](https://user-images.githubusercontent.com/85318060/137236197-12d603f4-d6ed-4ee5-a6c7-f4cc6029bf64.png)
I was then able to perform a count on each of these DataFrames to determine the total number of reviews that were vine reviews, and were not vine reviews. 
 - Total Vine Reviews: 1,080
 - Total non-vine reviews: 49,673
Through further filtering I was able to determine how many of each of the types of reviews were 5 star reviews.
 - Total 5-star vine reviews: 454
 - Total 5-star non-vine reviews: 23,043
Then it was simple math to determine the percentage of 5-star reviews for each type.
 - Percentage of 5-star vine reivews: 42.0%
 - Percentage of 5-star non-vine reviews: 46.4%

## Summary
Overall it does not appear that there is a positive bias for reviews in the vine program. There is actually a lower percentage of 5-star reviews at 42.0% compared to the 46.4% in the regular reviews. If given more time to perform analysis on this data I would do a 2-sample T-test on the overall star rating for each type of review to see if the average rating is overall higher for the vine reviews than for the regular reviews.
