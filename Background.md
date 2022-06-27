# Background
The prometheus depository was created on Sep 18, 2021 and was edited over six years by ten contributors. This report aims to understand the current structure of the depository and explains the aim of the algorithms and logic behind using them. It is important to mention that the author of this report is not one of the depository developers.

# Structure of the depository

## Overall structure of the depository

![alt text](https://raw.githubusercontent.com/ImanKhamis/ImanKhamis/main/Capture1.PNG " Logo Title Text 1")


## The Branches

The depository has three main branches: Python 3, Call Functions and New branch. Call Function Branch seems to be a copy of Python 3 Branch with a small edit. The Call Function Branch has an extra folder named “Call Function” under the following path: Call Function>Dwell>DwellML>DwellMl>Call Function. This call function folder “contains the source to automatically run all Machine Learning models and ANN for Dwell Analytics when new data is coming in.” This document will mainly focus on the Dwell files and Dwell algorithms.

### Python 3 Branch/Call Function Branch

![alt text](https://raw.githubusercontent.com/ImanKhamis/ImanKhamis/main/Capture.PNG " Logo Title Text 1")
It appears that the goal of the algorithms in the DwellML folder is to do the following:
1. Load the dataset 
2. Clustering the users 
3. Undergo predictive analysis of users (predicting next location for users best on different features) 
4. Discover patterns of behaviors (for example frequency of visits) 
5. Analyze the distance covered by user and anticipate the mode of transportation


### Notebooks Folder

Contains One notebook “Density based Clustering approach.ipynb” that requires dwellml algorithms to run.


### Vinamra Folder

Vinamra Folder seems to contain notebooks with testing (R&D) experiments with results.
Call Function Branch
Call Function branch is an attempt to reorganize the python3 path with an addition of a Call Function folder to call all the built predictive algorithms.


![alt text](https://raw.githubusercontent.com/ImanKhamis/ImanKhamis/main/Capture2.PNG " Logo Title Text 1")

Call Function>Dwell>DwellML>DwellMl>Call Function
This folder contains code of different algorithms creating predictive models (to predict person next location, based on the current location and other features); 
1. Linear Regression Model
2. Decision Tree Model
3. KNN_ Class Model
4. KNN_Reg Model 
5. ANN Model (this model takes more than 45 minutes to run)

The folder contains python file, a folder, Read Me:

1. Call_source.py (the final script)

	Each version folder contains the necessary files within the same directory to run on a local machine. Here, the necessary files are 		contained in a different directory and when called is not recognized (05/05/2021)
    
2. Version History/Call Function v1


    a. Dataset_ANN.csv (Data Set used in all models)
    b. PL_main.py (automatically run all ML model and ANN for Dwell analytics when new data comes) & (save the graph results on local machine)
    c. Lib.py (Includes Linear Regression Model, Decision Tree Model, KNN class Model, and KNN Reg Model)
    d. Lib2.py (This function performs ANN_model on the loaded data)
    e. Results.txt (to store the results of the model into the .txt file
    
    
## New_Branch Branch 

It seems as if this Branch was meant to reorganize the previous two branches.


![alt text](https://raw.githubusercontent.com/ImanKhamis/ImanKhamis/main/Capture3.PNG " Logo Title Text 1")

## API (Application Programming Interface)
Module containing all of the logic used in recommending content given a content pool and salient input parameters.

### Rest API

#### - resources > Util

Notebook: “This API Resource is responsible for returning the list of timezones available to choose from to allow time of day triggers for geofences and/or associated content.”

#### - resources > audiences

1. AudienceProfileCollection defines target customers by unifying and analyzing consumer buying behaviors. 
2. It includes read only queries against the Profile resource collection. All responses will be in json API format.
3. As well, it handles the updates to existing resources. 

#### Unit Tests
Includes Test_prometheus_endpoints.py.










