# PART A : MOTIVATION
Industry Context
STADIOalot is one of South Africa’s largest online retailers, with 4.1 million active customers and R38 billion in yearly revenue. However, its operating margin is only 1.9%, meaning the company makes about R1.90 in operating profit for every R100 of revenue. Its advertising business makes up 9% of total revenue and is highly profitable because it costs very little to run.

The Existing Challenge
At the current moment, sponsored products on STADIOalot’s search and category pages are mainly given to the highest bidders. The system does not focus enough on which products are most relevant to each customer. As a result, customers may see ads that do not match their interests, which can cause frustration and abandoned searches. Sellers may also get less value from their advertising spend, while STADIOalot loses potential advertising revenue.

Importance of Addressing the Problem
Improving ad relevance can help STADIOalot increase its advertising revenue and profit. Advertising costs very little to run, so most additional advertising income can become profit. Even a small increase in click-through and conversion rates could lead to a meaningful increase in profit. This project also supports the CEO’s 2030 strategy to make the storefront personal and the ads relevant.

Potential Contribution of Data Science
A data-driven ranking model can predict how likely a customer is to click on or buy a sponsored product. The model can use three years of clickstream data, including searches, product views, and items added to the basket. It can also use purchase history and product information.

The model will use this information to rank sponsored products based on how relevant they are to each customer, instead of ranking them mainly by how much sellers pay. This can help STADIOalot increase advertising revenue while improving the customer shopping experience.

# PART B : PROBLEM STATEMENT 

What Problem Exists?
STADIOalot has three years of customer and product data, including clickstream data, order history, and product information. However, sponsored products are still mainly ranked based on the bid amount.
The system does not make enough use of customer behavior and preferences. Important information such as search history, products viewed, previous purchases, and demographic information is not fully used to show each customer the most relevant ads.

Who Is Affected by the Problem?
This approach affects customers, sellers, and STADIOalot as a whole. Customers may ignore sponsored products or leave their searches because the ads are not relevant to them or what they are trying to purchase. Sellers may not get good value from the money they spend on advertising. STADIOalot may also lose potential advertising revenue. Showing customers irrelevant products repeatedly can also reduce customer trust and engagement.

What Data Are Available to Investigate the Problem?
STADIOalot has several types of data that can be used to study the problem which consists of:
- Clickstream and Search data (3 years): Includes customer searches, product views, items added to the basket, purchases, and abandoned sessions.
- Orders and Transactions data (6 years): Includes products bought, prices, promotions, payment information, dates and times, and customer details.
- Product Catalogue data (6 years): Includes product IDs, categories, product details, prices, sellers, images, and reviews.

What Is the Intended Purpose of the Study?
This project aims to build a personalized ranking model that predicts how likely a customer is to click on or buy a sponsored product.
The model will use customer behavior data, such as searches, product views, and items added to the basket. It will also use previous purchases and product information.
The model will then rank sponsored products based on how relevant they are to each customer, instead of ranking them mainly by how much sellers pay.

What Is the Intended Purpose of the Study?
This project aims to build a personalized ranking model that predicts how likely a customer is to click on or buy a sponsored product.
The model will use customer behavior data, such as searches, product views, and items added to the basket. It will also use previous purchases and product information.
The model will then rank sponsored products based on how relevant they are to each customer, instead of ranking them mainly by how much sellers pay.


Problem Statement Summary (One Sentence)
STADIOalot currently ranks sponsored products mainly by bid amount instead of relevance, so this study will use three years of customer behavior, order, and product data to build a personalized model that predicts which products customers are most likely to click on or buy, helping improve the customer experience and advertising revenue.


# STADIOalot-Capstone
Capstone project for STADIOalot
This repository is organized to keep all the files needed for the STADIOalot advertising project for our client to be able to review the necessary and required information. It supports the different steps of the data science project, from preparing the data to building and testing the model

datasets – this consists of the raw and cleaned data used in the project. If the files are too large, this folder can contain sample files or information about the data instead.
models – consists of the trained machine learning models, such as .pkl files, as well as information about different versions of the models.
experimental_setup – consists of the required settings used for the experiments. This includes model parameters, hyper parameter settings, cross-validation methods, and pipeline configurations.
experimental_results – consists of the results from the experiments. This may include performance scores such as AUC, NDCG, and accuracy, as well as confusion matrices and other experiment results.
statistical_scripts – consists of the scripts used for statistical tests, A/B testing, and checking that the data is correct and reliable.
visualisation_scripts – consists of the scripts for creating graphs and charts. These can include EDA graphs, feature importance charts, and visualizations used in the final report.
