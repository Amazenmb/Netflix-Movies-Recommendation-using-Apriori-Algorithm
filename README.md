# Netflix-Movies-Recommendation-using-Apriori-Algorithm
This is a recommendation system for movies on Netflix based on past movie watched dataset of users and using Apriori Algorithm's Association Rule learning, the next movie is suggested to the user.

 I have trained the model and implemented the recommendation system. It works similar to "You may want to watch X" , "People like you are watching Y".

**A bit about Apriori**

Apriori is a machine learning algorithm to identify relationships between items by identifying frequent itemsets. The process relies on the Apriori property that states that if an itemset appears frequently in a dataset, all its subsets must also be frequent. Some common use cases are to analyze clickstream data, identify fraudulent patterns in financial transactions, and recommendation systems like movies, articles, market basket analysis for ecommerce platforms, etc.

Metrics:
a) Support - ratio of the number of times an item occurs in the transactions to the total number of transactions

![image](https://github.com/user-attachments/assets/a17d8ec0-a528-40d0-81d4-5b2f76f8351e)

For example, let's say out of 1000 users who made the purchase on BigBasket, 150 people bought apples and 180 bought banana. 
Then, Support(Apples)= 150/1000 = 15%
And Support(Banana) = 180/1000 = 18%

We can indicate a required minimum support threshold when applying the Apriori algorithm. This means that any item or itemset with support less than the specified minimum support will be considered infrequent.

b) Confidence - identifies the probability of items or itemsets occurring in the itemsets together. 
![image](https://github.com/user-attachments/assets/64bf0121-3276-4755-9c9e-c59b34402937)

For exmaple, out of a set of 150 users who bought apple, people who bought banana is 80, therefore
Confidence(Apple ->Banana) = 80/150 = 53.3%

If out of 180 people who bought Banana, there were 60 who bought apple,
then Confidence(Banana -> Apple) = 60/180 = 33.3%

So, there is more likelihood of people buying banana after apple.

While confidence is a good measure of likelihood, it is not a guarantee of a clear association between items. Therefore, a minimum confidence threshold is applied to filter out weakly probable associations while mining with association rules.

c) Lift - factor with which the likelihood of item A leading to item B is higher than the likelihood of item A. This metric quantifies the strength of association between A and B. It can help indicate whether there is a real relationship between the items in the itemset or are they being grouped together by coincidence. 

![image](https://github.com/user-attachments/assets/cc598b73-a20f-4bb7-a858-ff1b07c33773)

For example,
L(Apples-> Bananas)= 53.3/15 = 3.5%
L(Banana ->Apple) = 33.3/18 = 1.9%

The high lift value of second case indicates that the likelihood of people buying bananas after apple is 2 times higher which also indicates that a banana purchase leading to an apple purchase might be just a coincidence.


**Data points(in dataset)**
Cart items of past purchases of a set of users


**Steps**
1. Import Libraries
2. Import Dataset
4. Set up Association Rule using Apriori
5. Evaluate the results

