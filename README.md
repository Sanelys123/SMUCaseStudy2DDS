# SMUCaseStudy2DDS
My Final Project for DDS Course

#To carry out wine quality prediction on a train dataset, I am going to follow these enumerated steps below:

#1.    Data Preparation

##1a.    Loading the Data Set: Import necessary libraries and load training dataset.
      
##1b.    Explore the Data: Understand the dataset structure, check for missing values, and examine the target variable (wine quality).
      
##1c.    Data Cleaning: Handle any missing values and remove duplicates if necessary.

#2.    Data Pre-processing

##2a.    Feature Selection: Identify and select relevant features that may affect wine         quality.

##2b.    Normalization/Standardization: Scale the features to ensure they are on a similar scale, which can be essential for some algorithms.(if required)

##2c.    Encoding Categorical Variables: If there are any categorical features, convert them into numerical format using techniques like one-hot encoding.

#3.     Splitting the Data

##3a.    If you have a validation set, split the training data into training and validation sets. This can be done using train_test_split from sklearn.

#4. Model Selection

##4a.    Choose a machine learning model appropriate for the task. Common algorithms for regression or classification tasks include:

##4b    For this Project, I am going to use these 2 regression model and select the model that predicted better for the testing data set. These models are;
##4b1.    Decision Trees
##4b2.    Multiple Linear Regression

#5.       Model Training

##5a.   Fit the model to the training data using the selected features and target variable.

#6.     Model Evaluation

##6a.   Evaluate the model's performance using appropriate metrics:

##6b.   For regression: I am going to employ Mean Squared Error (MSE), R² score. And for classification I will use Accuracy, and Recall.

#7.   Hyperparameter Tuning- I am not going to do hyperparameter tuning for this modelling.

#8. Make Predictions: I am going to use the trained model to make quality predictions on the provided test dataset.

################################
#CONCLUSIONS
################################
#1 EDA CONCLUSION
#Summary of Interpretation of ANOVA

#a. Location Effect: The results indicate a highly significant effect of location on wine quality (p < 0.001). This suggests that different locations produce wines of significantly different quality. But the dataset did not show what location. More in-depth work is required.

#b. Type Effect: The effect of wine type on quality is also significant (p < 0.05), indicating that the type of wine does have an impact on its quality, although this effect is not as strong as the location effect. We could not clearly see which of the type of wine had more quality based on the dataset.

#c. Interaction Effect: The interaction between location and type is highly significant (p < 0.001). This means that the effect of wine type on quality varies depending on the location, indicating complex relationships between these factors. As mentioned above, more wine data from California and Texas id required to do more in-depth work 

#d. Conclusion       	
#In conclusion, both location and type significantly influence wine quality, and their interaction suggests that the effect of type is not consistent across different locations. 
#This information can be valuable for winemakers and consumers alike, as it highlights the importance of both geographical and varietal factors in determining wine quality.

#2. CONCLUSION ON THE MODEL BUILT ON THE TRAIN DATA
#a. The comparison result of the models showed that both models predicted good on test data. There is no better models between the models I used according to my analysis.

#b. Since the analysis show that the results are both good, I will then use my subjective opinion to choose the model I will use on the "GIVEN" test data. I prefer MULTIPLE LINEAR REGRESSION.

#c. This is because of the feature importance result of the model, which is DENSITY. The feature result by RANDOM FOREST did not clearly stated a particular variable, but provided a clue that "location" is the most important feature. I do not know whether it is California or Texas. The dummy used did not explicitly splitted that variable into 2 columns for me to know exactly.

#d. Therefore, I have choosen to use MULTIPLE LINEAR REGRESSION as my model used to predict WINE QUALITY on the given test data of the project.

#e. The trained data was saved as a RDS file and included in my submission. This is used as trianed data for my Shiny App file, named "Wine Quality Prediction App.rmd".

#f. The Test Predicted Wine Quality was saved as a CSV file and included in my submission. This file is named "Wine Predicted Data.csv"
