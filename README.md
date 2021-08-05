# Amazon_Vine_Analysis
### Introduction- Overview of the analysis: Explain the purpose of this analysis.
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. In this project, the Pet Product dataset containing reviews willbe used with PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, PySpark, Pandas, or SQL will be used to determine if there is any bias toward favorable reviews from Vine members in the dataset. Last, a writen summary of the analysis will be submited to the SellBy stakeholders.



### Results: Using bulleted lists and images of DataFrames as support, address the following questions:

##### 1. How many Vine reviews and non-Vine reviews were there?
There were 38,010 helpful reviews. 

<img width="360" alt="Screen Shot 2021-08-05 at 9 41 49 AM" src="https://user-images.githubusercontent.com/82460401/128369487-f50f08f7-afc5-4795-a237-398f652f7893.png">

There were 170 paide reviews. 

<img width="360" alt="Screen Shot 2021-08-05 at 9 41 49 AM" src="https://user-images.githubusercontent.com/82460401/128370000-e3c46818-db49-404c-ba08-94dbda8ac850.png">

There were 37,840 unpaid reviews. 

<img width="480" alt="Screen Shot 2021-08-05 at 9 45 25 AM" src="https://user-images.githubusercontent.com/82460401/128370138-a0801fe2-ab24-4ddb-b496-12ca4bd6ebee.png">


##### 2. How many Vine reviews were 5 stars? 
Of the 170 paid reviews only 65 of them were 5 star reviews. 

https://www.tutorialspoint.com/logistic_regression_in_python/logistic_regression_in_python_quick_guide.htm

##### 3. How many non-Vine reviews were 5 stars?
Of the 37,840 unpaid reviews 20,612 were 5 star reviews. 

https://www.tutorialspoint.com/logistic_regression_in_python/logistic_regression_in_python_quick_guide.htm

##### 4. What percentage of Vine reviews were 5 stars? 
Roughly 38% of the paid reviews were 5 star.

https://www.tutorialspoint.com/logistic_regression_in_python/logistic_regression_in_python_quick_guide.htm

##### 5. What percentage of non-Vine reviews were 5 stars?
Roughly 54% of the unpaid reviews were 5 star. 

https://www.tutorialspoint.com/logistic_regression_in_python/logistic_regression_in_python_quick_guide.htm

### Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
Based on the descriptive data provided there does not appear to be a positive bias in the Vine program. The paid reviews make up less than 1% of all reviews and there is a smaller percentage(38%) of 5 star reviews from paid reviewers than un-paid reviews. The unpaid reviews make up 99% of all reviews and nealy half (54%) of those revies were 5 star.
Additionla analysis to support the conclusion that there is no positive bias in the paid reviews woudl be to evaluate the two groups at all ratings levels. All thought the data set is so heavily skewed towards un-paid reviews I doubt there will be much differnece. 

The next step in the analsyis of this data should be to group the data by 5 star reviews on product ID to evaluate which products may have more 5 star reviews. 


