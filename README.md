# Readme for CS771 Mini Project 1 - Group 67 Transformers
## Structure of Zip Submission
Along with our main transformers.py file, we have submitted the predictions for dataset 1, 2,3 and on the combined dataset whose names start with **pred**.
Additonally, we have attached some of the files which were relevant to the preprocessing performed by us on the datasets. 

### 64.py ###
The libraries/dependancies used are 
* Numpy
* Pandas 
* Sklearn
* Matplotlib
* re
* csv 
* xgboost
#### Running Instructions ####
To run Transformers.py, the datasets folder  in this parent folder names 67. Additonally the libraries above must be available in the enviromnment. The entire training and prediction could take around 
4 minutes depending on the system in use. 


#### Function Declarations and Defintions ####
* **fixDataframe(df)** : Separates the 13 emojis of dataset 1 into 13 separate columns. 
* **encode_dataset** : Performs one hot encoding on each input the dataset 1 by calling **encode_row** 
* **process_dataframes** : Removes the repeating substrings from dataset 3 while handling the case of overlapping substrings. 
* **evaluate_with_different_splits** : Takes in the combined preprocessed datasets and takes a certain perctange and then applies SVC (our best model according to tests)



For task 1, every dataset is loaded and pre-processed according to our earlier findings.
Following which the model which we found best is loaded with varying hyperparameters and then training followed by cross validation using GridSearchCV has been performed to get the best hyperparameters and results. 

## Resulting Accuracies (For the best models) ##
### 98.16% accuracy for dataset1 validation ### 
Logisitc Regression L1 Regularizer with C=100 and solver = Liblinear

Ourgraph mentions 97.75% to be the max accuracy but after including further hyperapramters in the GridSearchCV, the above was obatined. 
### 98.57% accuracy for dataset2 validation ###
 Random Forest Classifier with max_depth: 20, min_samples_split': 2, n_estimators: 200
### 86.71% accuracy for dataset3 validation ###
XGBoost :  lr=0.1, max_depth = 6, n_estimators = 1400 



## Other useful notebooks/files attached ##
**Decipher.ipynb** : After we discovered that every emoji of dataset 1 has a code corresponding in dataset 3, we decided to find the code for all the emojis. For this we had to come up with  a custom algorithm as given in the notbeook adn the codes appear at the end. 

**emoji_codes** : The codes for the emojis found. 
**Dataset1.ipynb** : This is the notebook we used to work on the 1st dataset which included finding patterns and feature dropping and training of subsequent models. 

**Datest1_rough.ipynb** :  This notebook has a subset of the analysis that we made on the dataset 1. This has been provided for additional information and is a rough work mainly meant for our usage for devleoping the final solution.


**Datest3_rough.ipynb** :  This notebook has a subset of the analysis that we made on the dataset 3. This has been provided for additional information and is a rough work mainly meant for our usage. 


### Backup_predictions ### 
This folder contains .txt files of prediciton which are a safety measure if in case the code doesn't execute properly on other systems