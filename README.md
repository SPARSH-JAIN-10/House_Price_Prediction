# Housing_Price_Prediction_In_Beijing

## Installation Guide
1. Clone or Fork the Project
2. Create a Virtual Environment
3. go to the same virtual environment and write below cmd
4. pip install -r requirements.txt

## Project Highlights
1. Research Paper
2. User Friendly
3. Accuracy
4. Open Source

## Table Of Content
1. [Project Descriptiom](https://www.kaggle.com/ruiqurm/lianjia)<br>
    A. Problem Statement<br>
    B. Best Possible Solutions<br>
    C. Introduction About Project<br>
    D. Tools and Libraries
2. [Data Collection](https://www.kaggle.com/ruiqurm/lianjia)
3.  Generic Flow Of Project
4. [EDA](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Housing_Price_Predication_Project_EDA.ipynb)<br>
    A. Data Cleaning<br>
    B. Feature Engineering<br>
    C. Data Normalization
5. [Choosing Best ML Model](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Machine_Learning_Model_Creation.ipynb)
6. [Model Creation](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Machine_Learning_Model_Creation.ipynb)
7. Model Deployment
8. Model Conclusion
9. Project Innovation
10. Limitation And Next Step
11. Working Project Video


### 1. Project Description
#### A. Problem Statement

Thousands of houses are sold every day. There are some questions every buyer asks himself like: What is the actual price that this house deserves? Am I paying a fair price?

#### B. Best Possible Solutions
a.Housing Expert<br>
b.Intuition About House<br>
c.Using Machine Learning

#### C. Introduction About Project
House Price predictions are very stressful work as we have to consider different things while buying a house like the structure and the rooms kitchen parking space and gardens. 
People don’t know about the factors that influence the house price.
But by using Machine learning we can easily find the house that is to be perfect for us and helps predict the price accurately.

#### D. Tools and Libraries
Tools<br><br>
a.Python<br>
b.Jupyter Notebook<br>
c. Flask<br>
d. HTML<br>
e. CSS<br>
f. JS<br>
g. Heroku<br>
h. GitHub

Libraries<br><br>
a.Pandas<br>
b.Scikit Learn<br>
c.Numpy<br>
d.Seaborn<br>
e.Matpoltlib<br>



### 2. Data Collection
For this project, we used the data that is available on Kaggle. ([click here for data](https://www.kaggle.com/ruiqurm/lianjia)). There are 26 columns and 318851 Rows. These are the major points about the data set.<br>
URL: the URL which fetches the data<br>
id: the id of transaction<br>
Lng: and Lat coordinates, using the BD09 protocol.<br>
Cid: community id<br>
tradeTime: the time of transaction<br>
DOM: active days of market<br>
followers: the number of people who follow the transaction.<br>
totalPrice: the total price<br>
price: the average price by square<br>
square: the square of house<br>
living: the number of living rooms <br>
drawing room: the number of drawing rooms <br>
kitchen: the number of kitchens <br>
bathroom the number of bathroom<br>
floor: the height of the house. I will turn the Chinese characters into English in the next version.<br>
building type: including tower( 1 ) , bungalow( 2 )，combination of plate and tower( 3 ), plate( 4 ).<br>
constructionTime: the time of construction<br>
renovationCondition: including other( 1 ), rough( 2 ),Simplicity( 3 ), hardcover( 4 )<br>
building structure: including unknown( 1 ), mixed( 2 ), brick and wood( 3 ), brick and concrete( 4 ),steel( 5 ) and steel-concrete composite ( 6 ).<br>
ladderRatio: the proportion between the number of residents on the same floor and the number of elevators of ladder. It describes how many ladders a resident has on average.<br>
elevator: have ( 1 ) or not have an elevator( 0 )<br>
fiveYearsProperty: if the owner has the property for less than 5 years.<br>

### 3. Generic Flow Of Project
![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/18.png)

### 4. EDA
![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/1.png)
#### A.Data Cleaning
we have 26 columns, from these we don't want some columns (i.e. URL, id,cid) then we will perform data cleaning which involves the following steps. our target variable is totalPrice<br>
a. Impute/Remove missing values or Null values (NaN)<br>
b. Remove unnecessary and corrupted data.<br>
c. Date/Text parsing if required.

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/2.png)<br>
we handle NAN value using appropriate solutions.

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/3.png)<br>
DOM Column which has more than 50% of values missing it's better to delete that column


![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/4.png)<br>
some columns have unique characters. we solve these problems using the split method and create separate columns for unique characters.<br>

We also have categorical data we handle such kind of data using dummy variable concept. following are the columns that have categorical data.<br>
a. renovationCondition<br>
b. buildingStructure<br>
c. buildingType<br>
d. district<br>
e. elevator<br>
f. floor_type

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/5.png)<br>
Summary of the Heat-Map<br>
a. totalPrice is highly correlated with community average, square, bathroom, living room, and Trde Time.<br>
b. total price is highly negatively correlated with ladderRatio, lat, and lng.

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/6.png)<br>
Summary of the Density Plot<br>
a. most of the output features lie between 0-2500

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/7.png)<br>
Summary of Scatterplot<br>
a. Most of the House Followers 0-400.

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/8.png)<br>
Summary of Scatterplot with respect to renovationCondition<br>
a. most of the expensive houses have HardCover as a renovation condition

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/9.png)<br>
Summary of lineplot<br>
a. Most of the people's average lies in 12500-150000 ...

#### B. Feature Engineering
we found an outlier in our data...

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/10.png)<br>
from the above figure, we can notice that we have an outlier present in our dataset.<br>
for outliers we can use the IQR method and after using the IQR method. Now, our data looks fine.
![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/11.png)



using feature engineering we got out of the top 30 features for totalPrice.
![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/12.png)

So, these are the top 20 features for our model<br>
a. tradeTime<br>
b. CommunityAverage<br>
c. square<br>
d. livingRoom<br>
e. bathRoom<br>
f. drawingRoom<br>
g. renovationCondition<br>
h. buildingStructure<br>
i. elevator<br>
j. constructionTime<br>
k. Followers

#### C. Data Normalization
Normalization (min-max Normalization)<br>
In this approach, we scale down the feature between 0 to 1

we have a numerical column where we can apply min-max Normalization.<br>
![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/13.png)

### 5. Choosing the Best ML Model
List of the model that we can use for our problem<br>
a. LinearRegression model<br>
b. KNN Model<br>
c. Decision Tree<br>
d. Random Forest


![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/14.png)<br>
Using the linear regression we got only 75 % accuracy.

![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/15.png)<br>
Using the Random Forest we got 98 % accuracy on train data and 89 % on test data .so, we can consider RandomForest as a  Best Algorithm for this problem.


### 6. Model Creation
So, using a RandomForest to get good accuracy, we can Hyperparameter tuning  for best accuracy.

Algorithms that can be used for Hyperparameter tuning are:-

a. GridSearchCV<br>
b. RandomizedSearchCV<br>
c. Bayesian Optimization-Automate Hyperparameter Tuning (Hyperopt)<br>
d. Sequential model-based optimization<br>
e. Optuna-Automate Hyperparameter Tuning<br>
f. Genetic Algorithm<br>

The main parameters used by RandomForest Algorithm are:-

a. n_estimators --->    The number of trees in the forest.<br>
b. criterion--->{"mse", "mae"}-->The function to measure the quality of a split<br>
c. max_features--->{"auto", "sqrt", "log2"}-->    The number of features to consider when looking for the best split:


So, After Hyperparameter Tuning we got 90 % accuracy on test data and 94 % accuracy on train data. 
![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/16.png)<br>
Now, the accuracy of the model seems to be very good so we can save the model using pickle. 


### 7. Model Deployment
After creating the model, we integrated that model with a beautiful UI. For the UI part, we used HTML, CSS, JS, and Flask.
![](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/17.png)

### 8. Model Conclusion

The model predicts 90% accurately on test data and 94% accurately on train data.


### 9. Project Innovation
a. Easy to use<br>
b. open source<br>
c. Best accuracy<br>
d. GUI Based Application

### 10. Limitation And Next Step
Limitation are :-<br>
a. Mobile Application<br>
b. Accuracy can be improved <br>
c. Model Size is heavy(~310 mb )<br>
d. Feature is limited

Next Step are:-<br>
a. we will work on mobile application<br>
b. we will reduce the size of the model using PCA.


### 11. Working Project Video
![Working Projecct](https://github.com/SPARSH-JAIN-10/House_Price_Prediction/blob/main/Picture_For_README/video.gif)
