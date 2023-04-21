# AMLC-2023 - Amazon ML Challenge 2023

## Problem: Product length prediction
The goal is to develop a machine learning model that can predict the length dimension of a product. Product length is crucial for packaging and storing products efficiently in the warehouse. Moreover, in many cases, it is an important attribute that customers use to assess the product size before purchasing. However, measuring the length of a product manually can be time-consuming and error-prone, especially for large catalogs with millions of products.

## Task:
Build a machine learning model that can predict product length from catalog metadata.

## Dataset: 
* train.csv: 2249698 x 6
* test.csv: 734736 x 5
* sample_submission.csv: 734736 x 2

The columns provided in the dataset are as follows:
* PRODUCT_ID - Represents a unique identification of a product
* TITLE - Represents the title of the product
* DESCRIPTION - Represents the description of the product
* BULLET_POINTS - Represents the bullet points about the product
* PRODUCT_TYPE_ID - Represents the product type 
* PRODUCT_LENGTH - Represents the length of the product

## Evaluation Metric:
score = max(0 , 100 * (1 - metrics.mean_absolute_percentage_error(actual,predicted)))


