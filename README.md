# e_commerce_classification_project
## Determine wether or not a future package will be delivered on time or not
## Business understanding:
  ### With the growth of the E-commerce market market Cap, there has been a growth of approximately 14 % over brick and mortar oppurations.  One of the driving factors for customer satisfaction is wether or not the package will be delivered when it is supposed to be.  If we say the package will be there on a given day, then it should be there on that day or before, if our timelines are not correct, then we need to adjust timelines and determine what the import factors are in determining if a package will be delivered on time or not.
## Data Utilized:
  ### We utilized the E-Commerce Shipping Data from kaggle, this data set has 10,999 entries and it includes:
  __ID__: ID Number of Customers.
__Warehouse block__: The Company have big Warehouse which is divided in to block such as A,B,C,D,E.<br>
__Mode of shipment__:The Company Ships the products in multiple way such as Ship, Flight and Road.<br>
__Customer care calls__: The number of calls made from enquiry for enquiry of the shipment.<br>
__Customer rating__: The company has rated from every customer. 1 is the lowest (Worst), 5 is the highest (Best).<br>
__Cost of the product__: Cost of the Product in US Dollars.<br>
__Prior purchases__: The Number of Prior Purchase.<br>
__Product importance__: The company has categorized the product in the various parameter such as low, medium, high.<br>
__Gender__: Male and Female.<br>
__Discount offered__: Discount offered on that specific product.<br>
__Weight in gms__: It is the weight in grams.<br>
__Reached on time__: It is the target variable, where 1 Indicates that the product has NOT reached on time and 0 indicates it has reached on time.<br>

### We utilized feature importance and inferential knowledge to determine which of these feature where most important to the target predictions.  We eliminated items like gender because it a nondetermination factor and customer care calls and customer ratings because these happen after the fact of the delivery.  Mode of shipment, warehouse block and product importance were eliminated because they came out as not carrying very much importance in the determination of wether or not the package would be delivered on time.

## Data Modeling:
### Initially we utilized a logistic regression analysis to help with the classification, but the results was only an accuracy of 66%
### We then experimented with SVM modeling which resulted in an accuracy score of 68%
### Not being satisfied with the results so far, we utlized Decission Trees, Random Forrest and K nearest neighbors to determine what the ideal parameters and features were, The initial results were wonderful and it appeared we had a perfect model, but it was overfit and when we ran the test data it resultsed in an accuracy of only 67%<br>We then utilized Decision Trees to determine feature importance and simplify the model, but the result was only an accuracy of 64%<br>We switched models and tried running a SVM model with the important features, this resulted in a model accuracy of 64%<br>The next model to be run was the Naive Bayes model and again we ended with model accurracy under 70%<br>The next idea was to run an xgBoost classifier and modeling and with this model we finally ended with a solid result it ended with a model accurracy of 84% for both test and Train sets, We increased our f1 scores to a 82% and an 86% for Not delivered on time and Delivered on time respectively.  Being that we have not had any models that have even come close to this result, we have determined to go with this result to predict if we were to deliver our product on time or not.
# Model Evaluation:
## Final model decision is to be the XGBoost model.
## The results of the model gave us a precision of 80% and only 265 false posative results, only 85 nfalse negative and false negatives will give us the most issues, because if we can predict that the product is going to be delivered late, then we can inform the customer and eleviate many of our unsatissfied customers by keeping them informed.  The biggest issue is when we beleive the product will be on time, but it ends up being delivered late.
# Conlusion:
## In conclusion we were able to come up with a workable model which gives a solid way to predict wether or not a package will arrive on time.  The final model gives us the ability to eliviate a lot of concern with the customer and to help them understand when a package will be delivered to them.  
## In the future I would like to increase the size of the data and add some time series data, so that we can see if the time of the year, week or day effect wether or not a package is delivered on time.  There is also the possibility of searching into the customer care calls and the customers rating using NLP and determine if the satisfaction or dissatisfaction is tied to the delivery of the product being on time or not on time
# Repository Structure

```
├── e_commerce_shipments.csv (data used for modeling)
├── E-commerce_project.pptx (images used in PPT and readme)
├── README.md : project information and repository structure
├── e_commerce_shipments.csv: (Presentation for Stakeholders)
└── e_commerce_project.ipynb (jupyter notebook used for modeling)
```
