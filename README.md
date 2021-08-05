
# Amazon_Vine_Analysis


![IMG_1309](https://user-images.githubusercontent.com/82460401/128375169-daa88f0f-552c-4058-930e-43cf960b251f.jpeg)


### Introduction- Overview of the analysis: Explain the purpose of this analysis.
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. In this project, the Pet Product dataset containing reviews willbe used with PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, PySpark, Pandas, or SQL will be used to determine if there is any bias toward favorable reviews from Vine members in the dataset. Last, a writen summary of the analysis will be submited to the SellBy stakeholders.

Data was pulled from the Amazon Vine website, loaded into the AWS server and connected to PG Admin and Google Colab notebook via PySpark was used to analyze the data. 

<img width="1237" alt="Screen Shot 2021-07-30 at 12 36 23 PM" src="https://user-images.githubusercontent.com/82460401/128374428-caf236f6-b102-4a5c-927e-fad340417ede.png">
<img width="1216" alt="Screen Shot 2021-07-30 at 12 47 46 PM" src="https://user-images.githubusercontent.com/82460401/128374432-dbceb2cf-40f8-48cb-9b9d-889957f04d78.png">
<img width="1946" alt="Screen Shot 2021-08-04 at 5 44 42 PM" src="https://user-images.githubusercontent.com/82460401/128374435-a389b715-6a2e-4e9b-8f70-ed4c6bbdd55f.png">
<img width="1726" alt="Screen Shot 2021-08-04 at 5 45 56 PM" src="https://user-images.githubusercontent.com/82460401/128374437-abfd334e-f71f-4704-90cc-97f76d4c9334.png">
<img width="1731" alt="Screen Shot 2021-08-04 at 5 46 23 PM" src="https://user-images.githubusercontent.com/82460401/128374438-a16aa3c1-9779-4e9b-9c0e-8fbd1a0af4e4.png">
<img width="1731" alt="Screen Shot 2021-08-04 at 5 47 47 PM" src="https://user-images.githubusercontent.com/82460401/128374441-b6e0a81c-53df-476c-9eb9-6ce59c8fb241.png">
<img width="1744" alt="Screen Shot 2021-08-04 at 5 48 19 PM" src="https://user-images.githubusercontent.com/82460401/128374442-22620cc1-ce44-41f1-aaf7-1ce92dc5f10e.png">



### Results: Using bulleted lists and images of DataFrames as support, address the following questions:

##### 1. How many Vine reviews and non-Vine reviews were there?
There were 38,010 helpful reviews. 

<img width="360" alt="Screen Shot 2021-08-05 at 9 41 49 AM" src="https://user-images.githubusercontent.com/82460401/128373804-12ed2da3-4bb5-45d8-8a29-09fe1201ab48.png">


There were 170 paide reviews. 

<img width="480" alt="Screen Shot 2021-08-05 at 9 45 25 AM" src="https://user-images.githubusercontent.com/82460401/128373631-ae76fbc0-2109-42dd-87d1-8d2737641424.png">


There were 37,840 unpaid reviews. 

<img width="522" alt="Screen Shot 2021-08-05 at 9 46 07 AM" src="https://user-images.githubusercontent.com/82460401/128373583-50dff742-6afe-4af5-a1c9-35fe5064f021.png">



##### 2. How many Vine reviews were 5 stars? 
Of the 170 paid reviews only 65 of them were 5 star reviews. 

<img width="831" alt="Screen Shot 2021-08-05 at 9 47 24 AM" src="https://user-images.githubusercontent.com/82460401/128373887-339d790f-b3df-4ce5-85be-9c3fd9a36496.png">

##### 3. How many non-Vine reviews were 5 stars?
Of the 37,840 unpaid reviews 20,612 were 5 star reviews. 

<img width="850" alt="Screen Shot 2021-08-05 at 9 48 39 AM" src="https://user-images.githubusercontent.com/82460401/128373946-f8f51fcc-6e88-4fe9-af34-63bc5a76f2e1.png">


##### 4. What percentage of Vine reviews were 5 stars? 
Roughly 38% of the paid reviews were 5 star.

<img width="775" alt="Screen Shot 2021-08-05 at 9 49 31 AM" src="https://user-images.githubusercontent.com/82460401/128373969-085d5d27-3861-4031-8e48-e6e6141212f7.png">


##### 5. What percentage of non-Vine reviews were 5 stars?
Roughly 54% of the unpaid reviews were 5 star. 

<img width="782" alt="Screen Shot 2021-08-05 at 9 50 22 AM" src="https://user-images.githubusercontent.com/82460401/128373990-b8fc474c-2838-450d-ab3c-d100361c9eee.png">



### Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
Based on the descriptive data provided there does not appear to be a positive bias in the Vine program. The paid reviews make up less than 1% of all reviews and there is a smaller percentage(38%) of 5 star reviews from paid reviewers than un-paid reviews. The unpaid reviews make up 99% of all reviews and nealy half (54%) of those revies were 5 star.
Additionla analysis to support the conclusion that there is no positive bias in the paid reviews woudl be to evaluate the two groups at all ratings levels. All thought the data set is so heavily skewed towards un-paid reviews I doubt there will be much differnece. 

The next step in the analsyis of this data should be to group the data by 5 star reviews on product ID to evaluate which products may have more 5 star reviews. 


