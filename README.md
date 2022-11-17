#Big Data Challenge

In this challenge were were asked to analysis two datasets from Amazon review data which was pulled from 
https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt

**Tech Stack:**
* Jupyter Notebook
* Python
* Pyspark (Spark Framework) - Google Colab
* AWS Postgres
* Hadoop Cluster

The sample selected were for EBOOKS https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Digital_Ebook_Purchase_v1_01.tsv.gz https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Digital_Ebook_Purchase_v1_00.tsv.gz

Sample columns for Ebook Dataset

<img width="880" alt="image" src="https://user-images.githubusercontent.com/75756974/201268536-8ca6791c-e5e9-434a-bfba-9c5b322cbbcb.png">

DATA COLUMNS:
* marketplace - 2 letter country code of the marketplace where the review was written. 
* customer_id - Random identifier that can be used to aggregate reviews written by a single author. 
* review_id - The unique ID of the review.
* product_id - The unique Product ID the review pertains to. 
* product_title - Title of the product. 
* product_category - Broad product category that can be used to group reviews (also used to group the dataset into coherent parts). 
* star_rating - The 1-5 star rating of the review. 
* helpful_votes - Number of helpful votes. 
* total_votes - Number of total votes the review received. 
* vine - Review was written as part of the Vine program. 
* verified_purchase - The review is on a verified purchase. 
* review_headline - The title of the review.
* review_body - The review text. 
* review_date - The date the review was written.


Processing Data
* Step 1:  Created database in AWS RDS Postgres Instance and Database  to hold data after processing
* Step 2: Created tables to hold data in AWS Progres RDS
* Step 3:  Created two separate notebooks for processing each dataset (music and ebooks)
* Step 4:  Performed ETL (Extracted CSV files, created dataframes for each data set, filtered data for processing, loaded data from each dataframe into AWS Postgres 
<img width="592" alt="image" src="https://user-images.githubusercontent.com/75756974/202345927-716c7256-8dac-47a0-885e-c7f8aedb2caf.png">

<img width="564" alt="image" src="https://user-images.githubusercontent.com/75756974/202345858-e3364f4b-acb6-4695-b410-bb70f5382d9e.png">

* Step 5: Verified Count of each dataset, first uploaded ebooks into database and then added music data for processing
<img width="429" alt="image" src="https://user-images.githubusercontent.com/75756974/202345727-55243924-9b10-406e-a223-16ed4f188de3.png">

Google Colab was used to create a notebook and process data: https://colab.research.google.com
