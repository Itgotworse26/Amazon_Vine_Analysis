# Amazon_Vine_Analysis
Challenge Assignment for Module 16

## Background 
Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.


## Overview
The purpose of this assignment is to determine if there is a bias towards postive reviews from Amazon Vine users. We are to determine if the fact that Vine allows manufacturers and publishers to send free products to Amazon Vine users affects the reviews that these users post. For this particular project, we are examining if the Amazon Vine affects reviews of video game products. 


## Results
As seen in the results below:

![Summary Dataframe](https://github.com/Itgotworse26/Amazon_Vine_Analysis/blob/main/analysis/summary_df.JPG)

In a summary of 5 Star reviews of video games sold by Amazon:

* There are 94 Amazon Vine reviews and 40,471 non-Amazon Vine reviews.
* 48 Amazon Vine reviews were 5 stars. 15,663 non-Amazon Vine reviews were 5 stars.
* About 51.06% of Amazon Vine reviews were 5 stars. About 38.7% of non-Amazon Vine reviews were 5 stars.

Meanwhile, in a summary of 1 Star reviews of video games sold by Amazon:

* Only 1 Amazon Vine review was 1 star. 10,303 non-Vine reviews were 1 star.
* About 1.06% of Amazon Vine reviews were 1 star. About 25.46% of non-Amazon Vine reviews were 1 star.


## Summary
The differences in amounts of five-star reviews between Amazon Vine and non-Amazon Vine users is about 13%. 

The differences are even more visible with one-star reviews. While only 1% of Vine users left one-star reviews, 25.46% of non-Amazon Vine users left one-star reviews.

There is an argument that could be made that for video games, Vine users definitely are more likely to leave positive reviews. For video game publishers, being able to send free proucts to Vine users most likely had an effect on the review scores if the gap between 5 stars and 1 star reviews are seen as above. 

Another analysis that I would recommend is an analysis of whether verified purchases affect star ratings. Being able to identify the number of verified purchases between Vine and non-Vine users and observing how it affects ratings should help identify whether Amazon's review scores are accurate and unbiased. Unfortunately, the difficulties of working with RDS means that pursuing this project on my own time would be difficult. RDS, while a powerful tool, is also comically finnicky and money-hungry, even in its supposedly "Free" tier, making it a terrible tool of choice for individual users. 