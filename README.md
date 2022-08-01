# Neural_Network_Charity_Analysis

## Overview of Project
Bek’s come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME**_AMT—Income classification
* **SPECIAL**_CONSIDERATIONS—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively

## Deliverables:
This new assignment consists of two technical analysis deliverables and a written report.

1. ***Deliverable 1:*** Preprocessing Data for a Neural Network Model
2. ***Deliverable 2:*** Compile, Train, and Evaluate the Model
3. ***Deliverable 3:*** Optimize the Model
4. ***Deliverable 4:*** A Written Report on the Analysis [`README.md`](https://github.com/DataJew/Neural_Network_Charity_Analysis)

## DELIVERABLE RESULTS:

#### Data Preprocessing
For this analysis and model, the target is held in IS_SUCCESSFUL field, which signifies if the money was used effectively.

##### The following variable(s) should be considered on features model

* NAME                      
* APPLICATION_TYPE             
* AFFILIATION                  
* CLASSIFICATION               
* USE_CASE                      
* ORGANIZATION                  
* STATUS                        
* INCOME_AMT                    
* SPECIAL_CONSIDERATIONS        
* ASK_AMT                    
* IS_SUCCESSFUL 

##### The following variable(s) should be removed from input and data.

* EIN

EIN (Employer identificaiton) was dropped because the numbers could confuse the system into thinking its significant.

##### Compiling, Training, and Evaluating the Model

**Model Configuration:**

* hidden_nodes_layer1 = 100
* hidden_nodes_layer2 = 30
* number_input_features = 10

In this model there are three hidden layers each with many neurons,  because this seeemed to increased the accuracy above 75%. The number of epochs wasn't changed. The first activation function was 'relu' but the 2nd and 3rd were 'sigmoid'and the output function was 'sigmoid'. Changing the 2nd and 3rd activation functions to 'sigmoid' also helped boost the accuracy. 


##### This model acheived 78.8% accuracy, slightly above the target model performance of 75%.
![image](https://github.com/DataJew/Neural_Network_Charity_Analysis/blob/main/Resources/images/optimized.png)


The folling steps were taken to increase model performance:

* Converting the NAME column into data points, which had the biggest impact on improving efficiency.
* Adding a third layer and using the "sigmoid" activation function for the 2nd and 3rd layer.


### SUMMARY

Overall, by increasing the accuracy above 75% we are able to correctly classify each of the points in the test data 75% of the time. Additionally, an applicant has approximately an 80% chance of being successful if they have the following:
- The NAME of the applicant appears more than 5 times (they have applied more than 5 times)
- The type of APPLICATION is one of the following; T3, T4, T6, T5, T19, T8, T7, and T10.
- The application has the following CLASSIFICATION; C1000, C2000, C1200, C3000 and C2100.

A good model to recommend is the Random Forest model because Random Forest are good for classification problems. Using this model produces a similar, 78% accuracy.
![image](https://github.com/DataJew/Neural_Network_Charity_Analysis/blob/main/Resources/images/RF.png)
