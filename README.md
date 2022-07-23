# Amazon_Vine_Analysis

# Project Purpose and Overview

The purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program to determine if there is any bias toward favorable reviews from Vine members in a particular dataset. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. For this project I have analyzed the Electronics dataset and used PySpark to perform the ETL process to extract, transform and load the dataset.  

# Results:

After analyzing the dataset we are able to uncover some key findings regarding the written reviews by members of the Amazon Vine program to determine if there is any bias toward favorable reviews from Vine members. Initially the dataset had over 3 million reviews written. Inorder to retreive the important reviews that can help with the analysis we filter the dataset. Firstly, we retreive all rows where total_votes coloumn count is equal to or greater than 20. After retreiving this information we calculate the percent of votes by retrieving all the rows where the number of helpful_votes divided by total_votes is equal to or greater than 50%. After these calculations we narrow down the number of reviews to 50, 739 which we can sort into dataframes to find the reviews that are written by Vine program members (paid) or Non-Vine program members (unpaid).

![s1](https://user-images.githubusercontent.com/100486461/180594989-cfc7b0c3-4302-49af-a036-35d52a85a616.PNG)
![s2](https://user-images.githubusercontent.com/100486461/180594990-5fa13671-f1e0-457f-9c02-6987c197d561.PNG)
![s3](https://user-images.githubusercontent.com/100486461/180594987-8181ab69-6ca7-431a-bda8-9998d9b942cb.PNG)
![s4](https://user-images.githubusercontent.com/100486461/180594988-1aa5ed85-7cea-4555-8d7b-dce29927e266.PNG)

To analyze the dataset furthur we determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).

- The current dataset has 50, 739 reviews in total written by Amazon Vine program and Non-Vine program members. There are 1080 reviews by Vine program members and 49, 673 reviews by Non-Vine members. 
- The total number of paid 5-star reviews is 454 and the total number of unpaid 5-star reviews is 23, 043. The percentage of 5-star reviews written by paid is approximately 42%, whereas the percentage of 5-star reviews written by unpaid members is 46%

![s6](https://user-images.githubusercontent.com/100486461/180595551-4abe38cd-1d27-4134-8df3-0678b6ccc83c.PNG)
![s5](https://user-images.githubusercontent.com/100486461/180595552-8677cc21-ecf2-4812-9ae2-001c711124b2.PNG)


# Summary:

Based on the summary reports we can tell that there is no bias in the reviews between the Vine and Non-Vine members. The percentage of 5-star reviews by both category members is almost the same.

- The total number of reviews is: 3093869
- The total number of paid reviews is: 1080
- The total number of unpaid reviews is: 49673
- The total number of 5-star reviews is: 1781156
- The total number of paid 5-star reviews is: 454
- The total number of unpaid 5-star reviews is: 23043
- The percentage of 5-star reviews for paid is: 42.03703703703704
- The percentage of 5-star reviews for paid is: 46.3893865882874

