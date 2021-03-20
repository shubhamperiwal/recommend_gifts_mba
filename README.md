# *Robust* Gifts Recommendation System

This project aims to build a recommender for a grocery store. It will recommend products based on your previous purchases as well as your current cart.

<b> Project origin - </b> The project originated while I was learning recommendation systems and was wondering how that works on a real-time basis when the products in my cart keep changing.

## Problem Statement

The main problem this project aims to solve is to build a dynamic robust recommender that provides personalized recommendations even for new users. Moreover, it uses Market Basket Analysis instead of product-similarity so it can be easily updated as items are added or removed from hypothetical cart


## Data Description

Source: http://archive.ics.uci.edu/ml/datasets/Online+Retail

This is a transnational data set that contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

### Attribute Information:

<b> InvoiceNo: </b> Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation. <br/>
<b>StockCode: </b>Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.<br/>
<b>Description: </b>Product (item) name. Nominal.<br/>
<b>Quantity: </b>The quantities of each product (item) per transaction. Numeric.<br/>
<b>InvoiceDate: </b>Invice Date and time. Numeric, the day and time when each transaction was generated.<br/>
<b>UnitPrice: </b>Unit price. Numeric, Product price per unit in sterling.<br/>
<b>CustomerID: </b>Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.<br/>
<b>Country: </b>Country name. Nominal, the name of the country where each customer resides.<br/>

## Model Information

<ul> Libraries used 
  <li> Basic EDA and analysis - pandas, numpy, matplotlib </li>
  <li>Market Basket Analysis - mlxtend </li>
  <li>Recommendation System - native python and pandas </li>
  <li> Model Evaluation - sklearn </li>
</ul>

It uses the following recommendations:

- New User - empty cart - Recommend popular products
- New User - items in cart - Market Basket Analysis to recommend products
- Old User - User user recommendations

## Summary of results

![Screenshot 2021-03-20 at 3 54 29 PM](https://user-images.githubusercontent.com/24404521/111863124-8f766c00-8994-11eb-972a-305c0b6edb60.png)
We can notice a trend of number of gifts increasing towards the second half after October in preparation for the holiday season.
And the trend finally peaks in early December when people have their Christmas shopping

![Screenshot 2021-03-20 at 3 56 58 PM](https://user-images.githubusercontent.com/24404521/111863176-e8460480-8994-11eb-8463-62e4807ce8db.png)
<i>`WORLD WAR 2 GLIDERS ASSTD DESIGNS` is the most popular products purchased </i>

![Screenshot 2021-03-20 at 3 56 30 PM](https://user-images.githubusercontent.com/24404521/111863166-d82e2500-8994-11eb-9c93-367696fef3a7.png)
<i>Here we can see rules for some of the products</i>

Results of recommendations for a selected user: <br/>
User selected - 13299 || Most similar user returned - 14156

- Products purchased by selected user - ['NATURAL SLATE CHALKBOARD LARGE', 'NATURAL SLATE HEART CHALKBOARD', 'PICNIC BASKET WICKER LARGE', 'ROSES REGENCY TEACUP AND SAUCER', 'ROUND SNACK BOXES SET OF4 WOODLAND']

- Products recommended - ['10 COLOUR SPACEBOY PEN' '12 COLOURED PARTY BALLOONS',  '12 EGG HOUSE PAINTED WOOD' '12 IVORY ROSE PEG PLACE SETTINGS',  '12 MESSAGE CARDS WITH ENVELOPES']

- Products purchased by most similar user - ['NATURAL SLATE CHALKBOARD LARGE' 'NATURAL SLATE HEART CHALKBOARD',  'PICNIC BASKET WICKER LARGE' 'ROSES REGENCY TEACUP AND SAUCER',  'ROUND SNACK BOXES SET OF4 WOODLAND']

`Therefore, we can see that user 14156.0 is most similar to user 13299 because 14156 has purchased ALL the same products as user 13299`

## Acknowledgements

1. Udacity Nanodegree Programme: https://classroom.udacity.com/nanodegrees/nd025/dashboard/overview
2. Article talking about Market Basket Analysis: https://pbpython.com/market-basket-analysis.html
3. Data: http://archive.ics.uci.edu/ml/datasets/Online+Retail
