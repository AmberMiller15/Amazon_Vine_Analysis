# Amazon_Vine_Analysis

### Overview 
- The purpose of this project was to take a set of data from the Amazon Product Review site and complete an analysis on the data, I chose data on Digital Ebook reviews. The first part of the analysis was to extract, transform, and load the data into postgresql using AWS and PySpark in a GoogleColab notebook. The data tables created the following during the ETL process:
    - A customers table outlining the customer_id and their review counts 
    - A review id table containing the review_id, customer_id, product_id, product_parent, and review_date columns
    - A products table containing the product_id and product_title
    - a vine table containing containing the review_id, star_rating, helpful_votes, total_votes, vine, verified_purchase columns

- After completing the ETL process analysis of review bias was analyzed compairing paid (vine) and unpaid reviews. In order to compare paid reviews and unpaid reveiws, a new data frame was created in a new Google Colab notebook and this dataframe was then used to create a filter dataframe containing 5 star reviews with 20 or more votes and helpful vote percentage greater than 50%. This dataframe was then separated out into paid review and upaid reviews. With the final anlaysis done on the final paid and unpaid dataframes to answer the following questions: 
    - How many Vine reviews and non-Vine reviews were there?
    - How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    - What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

### Results
- The Results as follows:
    - Total number of paid reviews are 0 for Digital Ebooks.
    
    ![image](https://user-images.githubusercontent.com/111200771/216173951-8bb18560-de29-4c90-85fb-a3268b98aa06.png)

    
    - Since the total number of paid reviews is 0 the total number of paid 5 star reviews and the percentage of 5 star paid reviews is also 0.
    
    ![image](https://user-images.githubusercontent.com/111200771/216174043-1eca3286-1513-4fb7-a680-b0b8567c7402.png)

    - The total number of unpaid reviews is 65149 reviews.
    
    ![image](https://user-images.githubusercontent.com/111200771/216174095-35fdb3e3-d8d4-49cd-8c87-1d5476398a4f.png)

    - The total number of unpaid 5 star reviews is 24673 reviews.
    
    ![image](https://user-images.githubusercontent.com/111200771/216174153-235b188b-871d-48fe-a4ef-78cdf34a4d03.png)

    - The percentage of unpaid 5 star reviews is 37.87% of the unpaid reviews. 
    
    ![image](https://user-images.githubusercontent.com/111200771/216174193-bc8bc8b1-75bc-4d75-9453-b030f4a70981.png)

    - Total number of reviews (both paid and unpaid) from unfiltered data is equal to 5101693 reviews.
    
    ![image](https://user-images.githubusercontent.com/111200771/216174240-e0b75689-391d-47d6-82f7-fd0ae35c5e78.png)
    
    - Total number of 5-star reviews from the unfiltered data is equal to 2952613 reviews.
    
    ![image](https://user-images.githubusercontent.com/111200771/216174288-dc8f934e-3860-4937-b8c9-39857be8e789.png)

    - The total percentage of 5-star reviews from the unfiltered data is 57.88%.
    
    ![image](https://user-images.githubusercontent.com/111200771/216174324-18fd91ea-ce74-4008-93c0-80fdba98a17e.png)

### Summary
- There is not a positivity bias for reviews in the Vine program for Digital Ebooks within this dataset. There were no paid reviews that left a 5 star rating for any of the Ebooks with more than 20 votes and the helpful_votes was at least 50 percent of the total_votes. The five star reviews in the final filtered data came from non-paid reviews. 
- An additional analysis that should be done on this data is an analysis of the total data and the percentage of 5 star reviews, which has been completed, and show above. 
