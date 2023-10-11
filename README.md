# FoodHub Data Analysis

## Introduction
The number of restaurants in New York is increasing day by day. Many students and busy professionals rely on those restaurants due to their hectic lifestyles. Online food delivery service is a great option for them. It provides them with good food from their favourite restaurants. A food aggregator company FoodHub offers access to multiple restaurants through a single smartphone app.

The app allows restaurants to receive a direct online order from a customer. The app assigns a delivery person from the company to pick up the order after the restaurant confirms it. The delivery person then uses the map to reach the restaurant and waits for the food package. Once the food package is handed over to the delivery person, he/she confirms the pick-up in the app and travels to the customer's location to deliver the food. The delivery person confirms the drop-off in the app after delivering the food package to the customer. The customer can rate the order in the app. The food aggregator earns money by collecting a fixed margin on the delivery order from the restaurants.
## Objective of this analysis
The food aggregator company has stored the data of the orders the registered customers made in their online portal. The aim of this analysis is to get a fair idea about the demand of different restaurants which will help them in enhancing their customer experience.
## Analysis
Import the required library
<img src="Required Library.PNG">

## Understanding the structure of the data
* Observation: The DataFrame has 9 columns. Data in each row corresponds to the order placed by a customer.
<img src="Read data.PNG">

### Question 1: How many rows and columns are present in the data?
* Observation: We have 1898 rows and 9 columns in our dataset
<img src="Question 1.PNG">

### Question 2: What are the datatypes of the different columns in the dataset?
* Observation: We have 4 integers, 4 objects and 1 float datatype in the dataset. The rating column should be an integer not object as seen in the dataset and this is because there is "Not given'. This will be changed as we dive deeper into the dataset.
<img src="Question 2.PNG">

### Question 3: Are there any missing values in the data? If yes, treat them using an appropriate method.
* Observation: There are no missing values in the dataset.
<img src="Question 3.PNG">

### Question 4: Check the statistical summary of the data. What is the minimum, average, and maximum time it takes for food to be prepared once an order is placed?
* Observation: For preparation time the min is 20 minutes, the average is 27.37 minutes and the max is 35 minutes.
* For cost, the minimum cost is 4.47, the mean is 16.498851, and the max cost is 35.41.
* For delivery time, the min is 15 minutes, the mean is 24.16 minutes, and the max is 33 minutes.
* For cost, 25% of observations are 12.08 and below, it takes 23 minutes or below to prepare and 20 minutes or below to deliver.
* For cost, 50% of observations are 14.14 and below, it takes 27 minutes or below to prepare and 25 minutes or below to deliver.
* For cost, 75% of observations are 22.2975 and below, it takes 31 minutes or below to prepare and 28 minutes or below to deliver.
<img src="Question 4.PNG">

### Question 5: How many orders are not rated?
* Observation: 736 orders were not rated
<img src="Question 5a.PNG">
* Convert rating from object to integer, so we first convert the string "Not given" to an integer
<img src="Question 5b.PNG">
* To drop the Order ID and Customer ID column
<img src="Question 5c.PNG">
<img src="Question 5d.PNG">

### Descriptive statistics for categorical columns(objects datatype)
<img src="Question 5e.PNG">

# Exploratory Data Analysis (EDA): Univariate Analysis
### Question 6: Explore all the variables and provide observations on their distributions. (Generally, histograms, boxplots, countplots, etc. are used for univariate exploration.)
<img src="Question 6a.PNG">
<img src="Question 6b.png">
* Observation: American Cuisine had the highest count
<img src="Question 6c.PNG">
<img src="Question 6d.png">
* Observation: We have the highest orders on weekends as against the weekday
<img src="Question 6e.PNG">
<img src="Question 6f.png">

### Question 7: Which are the top 5 restaurants in terms of the number of orders received?
<img src="Question 7.PNG">

### Question 8: Which is the most popular cuisine on weekends?
* Observation: American cuisine type is the most popular cuisine on weekends.
<img src="Question 8.PNG">

### Question 9: What percentage of the orders cost more than 20 dollars?
* Observation: 29.24% of total orders cost more than 20 dollars.
<img src="Question 9.PNG">

### Question 10: What is the mean order delivery time?
* Observation: The mean order delivery time is 24 minutes
<img src="Question 10.PNG">

### Question 11: The company has decided to give 20% discount vouchers to the top 5 most frequent customers. Find the IDs of these customers and the number of orders they placed.
* Observation: The fifth highest order count has 4 customer of 7 orders. It means there is a tie between the 5th to the 8th order_id
<img src="Question 11.PNG">

### Multivariate Analysis
### Question 12: Perform a multivariate analysis to explore relationships between the important variables in the dataset.
* Observation: From the correlation map, it shows that there is a weak correlation between the variables.
<img src="Question 12a.PNG">
<img src="Question 12b.png">
* Observation: American cuisine had the highest orders on the weekend followed closely by the Japanese cuisine
<img src="Question 12c.PNG">
<img src="Question 12d.png">

### Question 13: The company wants to provide a promotional offer in the advertisement of the restaurants. The condition to get the offer is that the restaurants must have a rating count of more than 50 and the average rating should be greater than 4. Find the restaurants fulfilling the criteria to get the promotional offer.
* Observation: Just 4 restaurants met the criteria.
<img src="Question 13.PNG">

### Question 14: The company charges the restaurant 25% on the orders having cost greater than 20 dollars and 15% on the orders having cost greater than 5 dollars. Find the net revenue generated by the company across all orders.
* Observation: The net revenue generated across all orders is $6166.3
<img src="Question 14.PNG">

### Question 15: The company wants to analyze the total time required to deliver the food. What percentage of orders take more than 60 minutes to get delivered from the time the order is placed? (The food has to be prepared and then delivered.)
* Observation: The percentage of orders that take more than 60 minutes to get delivered from the time the order is placed is 10.54%
<img src="Question 15.PNG">

### Question 16: The company wants to analyze the delivery time of the orders on weekdays and weekends. How does the mean delivery time vary during weekdays and weekends?
* Observation: The mean delivery time during the weekday is 28.34 minutes and the weekend is 22.47 minutes
<img src="Question 16.PNG">

