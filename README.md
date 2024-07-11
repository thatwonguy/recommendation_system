# Recommendation Systems Business Use-Cases
This repo demonstrates a product recommendation machine learning model for e-commerce like amazon products.

The notebooks demonstrating the code are the following:
1. `collab-filtering.ipynb`
   
    This notebook will utilize the `surprise` library to perform collaborative filtering to build a recommendation system based on past user purchase and viewing history. Reference this generic approach to understand how to implement a recommendation system in python to solve e-commerce business use-cases, etc.
2. `Product_Recommendation_System.ipynb`

    This notebook uses the `scikit learn` library along with a few other libraries to carry out and demonstrate additional approaches to compliment and build upon the first approach further, and uses the case-study of amazon products and users interacting and past purchase history of amazon products.

---

## 1. Generic solution to build recommendation system 

Reference `collab_filtering.ipynb` for using collaborative filtering when we have past user purchase and viewing history available.

In this notebook we use the `surprise` librariy, which is a simple and effective library for building and testing recommender systems.

1. First we install the necessary libraries in a venv or utilize dockerfiles:
```
pip install scikit-surprise
```
2. Next we:  
    - Carry out preliminary cleaning, EDA and prepping, creating and evaluation of model and do the following typically:
        1. bring in the data  
        2. define the reader with expected format  
        3. load data from dataframe (python or pyspark for larger data)  
        4. split the data into training and testing set  
        5. use a relevant algorithm lik KNN for collaborative filtering  
        6. train the algorithm/machine learning model on the train set  
        7. test the machine learning model on the test set  
        8. obtain some kind of metric, like rmse (root mean square error) to obtain base-line metric for   how well the model performed  
        9. at this point you can save the model in a proper format (i.e pickle file) 
    - Take the pickle file and reference it to do the following and build potential API layers with the following starting-point functions:  

        10. create a function to get top N recommendations for a given user

---

## 2. Problem Statement - Amzon-Product-Recommendation

Building recommendation system for products on an e-commerce website like Amazon.com.

### Description
Online E-commerce websites like Amazon, Filpkart uses different recommendation models to provide different suggestions to different users. 

Amazon currently uses item-to-item collaborative filtering, which scales to massive data sets and produces high-quality recommendations in real time. This type of filtering matches each of the user's purchased and rated items to similar items, then combines those similar items into a recommendation list for the user. In this project we are going to build recommendation model for the electronics products of Amazon. 

### References
The dataset here is taken from the below website. 

Source - Amazon Reviews data (http://jmcauley.ucsd.edu/data/amazon/)  The repository has several datasets. For this case study, we are using the Electronics dataset.
