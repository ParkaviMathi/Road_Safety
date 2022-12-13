# Road_Safety Analysis

## Project Title - Analysis of Road Crashes in South Australia from 2012 to 2021

In this project we look into the history of crashes that took place over the period from 2012 to 2021 in South Australia and create a Data Model to predict whether a crash would be fatal or non-fatal.

## Sources of Data


We are using data from the South Australian Government Data Directory:
https://data.sa.gov.au/data/dataset/road-crash-data/resource/1057e9ae-4672-4123-9c1d-1877483da401 and using the csv files from 2012_DATA_SA_Crash to 2021_DATA_SA_Crash

### Modifications
The csv files were combined to get a larger data set to ensure accuracy of the Data Model exceeds 75%. However, with the current data set we were able to achieve accuracy of 68%.

## Output Data out of this analysis

1. The number, types of crashes and if weather or time of day affects the type or number of crashes
2. The areas showing the highest number of crashes
3. The trend of the crashes over the years 2012 to 2021

## Contents of the Folders
1.  Resources: data sets of the crashes 
2.  Images: Images related to readme files
3.  Project_4_Presentation: Presentation file
4.  Project_4_Report: Project Report

## Team Members  	

Parkavi Jayachandran,
Balvinder Rajbans

## Dataset Tables - Raw

## Applications used:

Python - Libraries: Pandas, SQLite3, Tensorflow, Scikit-Learn, Numpy, Glob

Google Colab

Database - SQLite

Tableau 

## Process:

### Extract : 
The dataset is sourced from the South Australian Government Data Directory. The Master Zip file contains data in form of CSV  for Crash, Casuality and Unit from year 2012 to 2021.

### Transform:
The crash dataframe is created by reading into the crash csv file and the extraction of data is processed and additional columns not required are dropped.
The extracted data is stored in a new Dataframe ‘crash_df_filtered_1’ and will be used to load into the database.

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Data%20Set.png)

### Data Analysis:

As the Dataframe is now cleaned and transformed ready to be loaded into the machine learning model, the Deep Neural Network Model is used to predict the accuracy of the Target variable classification.

The scaled and transformed data is then passed through the neural network model, the number of input features and the hidden node in each layer is defined. 

Two hidden layers are added to the Neural network with the ‘ReLu’ activation function.

‘Softmax’ is used as the activation function for the Output Layer with 4 output units as per the unique values in ourTarget column.

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Model%20sequential.png)

The model is then trained using the fit-model function with the number of epochs set to 10.

The model_loss and model_accuracy is then calculated using the nn.evaluate function.

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/nn.evaluate%20function.png)

The model was then trained by tuning the hyperparameters to see if the accuracy can be increased but no further improvement was found with the given dataset.

## Visualisations:
Public Tableau has been used to generate all the visualisations.

#### 1. Number of crashes in South Australia from 2012-2021

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Number%20of%20Crashes%20in%20South%20Australia%202012-2021.png)
    
#### 2. Number and Type of crashes in South Australia from 2012-2021

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Number%20and%20Type%20of%20crashes%20in%20South%20Australia%20from%202012-2021.png)

#### 3. Crashes during Day Vs Night in South Australia 2021

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Crashes%20during%20Day%20Vs%20Night%20in%20South%20Australia%202021.png)

#### 4.	Number and Type of Crashes depending on Weather in South Australia 2021

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Number%20and%20Type%20of%20Crashes%20depending%20on%20weather%20in%20South%20Australia%202021.png)

#### 5.	Suburbs with over 150 Crashes in South Australia

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Suburbs%20with%20over%20150%20Crashes%20in%20South%20Australia%202021.png)

#### 6.	Map Showing Crashes in South Australia 2021

![chart](https://github.com/ParkaviMathi/Road_Safety/blob/main/Images/Map%20Showing%20Crashes%20in%20South%20Australia%202021.png)

## Project Report:
To access the detailed process of Extract, Transform, Analyse and Visualisations follow the steps shown in the Project Report.

