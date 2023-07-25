# Datasheet

- This Online Retail data was downloaded from UCI Machine Learning Repository https://doi.org/10.24432/C5BW33 (2015)

## Motivation

- This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail company
- The company mainly sells unique all-occasion gifts; Many customers of the company are wholesalers
- The data was donated to UCI in 2015 and allows for the sharing and adaptation of the datasets for any purpose, provided that the appropriate credit is given


## Composition

- The dataset contains transaction data occcuring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail company
- There are 541909 instances included with 8 attributes each
- Each instance contains a transaction / ordered item, for which the customer ID, invoice number, quanity, price etc. is given
- There are some missing values (CustomerID 135080 and Description 1454)

## Collection process

- The time frame of the data collection was between 01/12/2010 and 09/12/2011 and the data was donated by the company itself in 2015 

## Preprocessing/cleaning/labelling

- The included dataset is in the original state
- In the course of the code, some cleaning was done such as missing values were dropped as well as cancellations
- New variables (Frequency, Recency, Revenue per CustomerID) were calcuated to proceed with RFM analysis in the course of the code

## Uses

- In this analyis, the data is used for a RFM (recency, frequency, monetary) analysis but different sort of classicifation/clustering based on e.g. products can be conducted
- 

## Distribution

- This dataset is licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license
- This dataset is publicly available
