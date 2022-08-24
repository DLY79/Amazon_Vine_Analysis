# Amazon Vine Reviews Analysis  

## Summary  

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

Using Amazon music review data, we use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we used Pandas to determine if there is any bias toward favorable reviews from Vine members in your dataset. 

## Results

How many Vine reviews and non-Vine reviews were there?  
For this particular data set, there was only 7 reviews from people in the Vine program, and 105,979 reviews from non-Vine participants.
![Screen Shot 2022-08-24 at 12 56 36 PM](https://user-images.githubusercontent.com/103051630/186465638-59853092-97c1-4033-bd49-ed7f2bcc2d47.png)

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?  
Total 5 star reviews came from non_Vine reviews.  This means that all 67,580 5 star reviews in this data set were from non-Vine users.  
![Screen Shot 2022-08-24 at 1 14 31 PM](https://user-images.githubusercontent.com/103051630/186469668-2be5e613-42fd-458a-a482-2b0f684c5ef5.png)

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?  
Of the 105,979 reviews left by non-Vine shoppers, approximately 64% were 5-star reviews.  Of the 7 reviews from the Vine program, 0% left 5 star reviews.
![Screen Shot 2022-08-24 at 1 18 46 PM](https://user-images.githubusercontent.com/103051630/186470505-f9c43571-c159-4fc1-b612-250b1e796532.png)

## Conclusion  
Based on this analysis, it does not appear that the Vine program creates favourable bias.  To the contrary, reviews were lower.  This has been determined from only assessing the Music dataset, and more research is needed to determine this conclusively.

No data in this single dataset is given to suggest if the Vine shopper is more discriminate, however we could anecdotally suggest that they are, given that 64% of non-Vine customers felt they received 5 star products.  If likes, standards, expectations, and interests were all considered basically equal, we would expect about 4 of the 7 reviewers to give a 5 star review.  Further analysis of all data sets could give us a deeper understanding.

Although we could not look deeper in to the Vine user reviews, we could search further in to non-Vine users and eliminate the non-verified purchases.  This would reduce the data size, and would give us more reliable data to rely on.  

