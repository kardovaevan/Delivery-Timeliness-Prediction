# Delivery-Timeliness-Prediction

## Objective 
E-Commerce plays a significant role in our world nowadays. Objective of this project is to provide analysis of what variables affect the delivery of goods will be on time or not, and to predict if the shipments were delivered on time or not using Supervised Machine Learning.

## Data Explanation 
source : https://www.kaggle.com/prachi13/customer-analytics

The data contains the following information:
1. ID: ID Number of Customers.
2. Warehouse block: The Company have big Warehouse which is divided in to block such as A,B,C,D,E.
3. Mode of shipment:The Company Ships the products in multiple way such as Ship, Flight and Road.
4. Customer care calls: The number of calls made from enquiry for enquiry of the shipment.
5. Customer rating: The company has rated from every customer. 1 is the lowest (Worst), 5 is the highest (Best).
6. Cost of the product: Cost of the Product in US Dollars.
7. Prior purchases: The Number of Prior Purchase.
8. Product importance: The company has categorized the product in the various parameter such as low, medium, high.
9. Gender: Male and Female.
10. Discount offered: Discount offered on that specific product.
11. Weight in gms: It is the weight in grams.
12. Reached on time: It is the target variable, where 1 Indicates that the product has NOT reached on time and 0 indicates it has reached on time.

## Data Cleansing
The data does not contain major issues (No missing values and duplicated rows)

## Data Understanding
After checking the correlation for each variables against the target variable. Some variables need to be excluded. These are some variables used in the model: Warehouse block, Mode of shipment, Cost of the product, Product importance, Discount offered, Weight in gms

## Modelling
We will use 4 models:
1. Decision Tree as baseline model
2. Random Forest
3. AdaBoost
4. Gradient Boosting

Based on the analysis, Gradient Boosting appears to be the model with the best AUC scoring

## Feature Importance 
Using dalex to find the feature importance it turned out that discount offered is the most important variable followed by weight of the goods and cost of the product

## Recommendations 
1. Discounts are the most influential variable on the timeliness of delivery, highly recommend that future campaign is to give more below 10% discount compared to others
2. there is an interesting pattern on the weight of the products. where many items tend to arrive on time if the weight is below 2 kilograms and between 4-6 kilograms. It would be better if the company is also able to deliver goods on time for other weights.
3. Customers are more likely to reach CS when they buy products at relatively expensive prices. It is expected that the company and partners can improve the tracking system. So that customers can check the delivery process in real time
4. The delivery method has no effect on the timeliness of delivery. however, it is expected that company and partners can try to add express delivery alternative so that the products can arrive on time.
