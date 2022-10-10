# Web-Scraping-in-R
Extracting Amazon product names using ASIN codes from Google

This project automates a web scraping robot that googles ASIN codes from a dataset of Amazon video game products in order to store the respective product names. This is used within a wider project that aims to analyse the impact of several text-derived features from product reviews on the overall rating score of the product. The wider project considers features such as the sentiment associated with a review, the length of the review, readability, repeated words etc. This part of the project is concerned with investigating whether mentioning the product name within the text of the review has any impact on the overall score. 

The product names data was missing from the initial meta-data so the alternative solution was to scrape them from the web. A logical variable was then created that tracks whether the text of each review contains the name of the product. This is subsequently inputed into a logistic regression that reveals that mentioning the product name within the review has a significant positive (coeff=0.048) impact on the overall score granted by the reviewer. 

The code uses the Rselenium package and runs without the need for user interaction - capcha avoidance was done by incorporating a pause & error catching pattern into the code aimed to mimic human behaviour. 
