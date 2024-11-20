# Sales and Volume Forecasting model for for UK based online wholesale retailer selling globally
## Description
### In this project, we used data collected from UCI repository, this data represents sales transactions for an online wholesale retailer from 2011 to 2012
### For this project, we explored the dataset using visualization, and then prepared the data for forecasting sales dollars and quantity
### We visualized the variation of sales dollars and quantity with time (date) and decomposed time series data to extract trend, seasonality and noise
### We developed two optimal RNN models to forecast sales dollars (revenues) and sales quantity, by tuning the following hyperparameters to have the lowest RMSE
#### Look back period - 7, 30, 90 days
#### Number of units - 32,64, 128, 256
#### Batch size - 16,32,64

## Key findings
### Sales quantity - time series characteristics
#### Quantity overall had a positive trend from 2011 to 2012
#### Sales quantity seasonality was pronouced every 30 days (ACF plots), seasonality diminished if we extended over 90 days
#### Sales quantity did not have seasonality over a weekly duration
### Sales revenue (dollars) - time series characteristics
#### Sales revenue overall had a positive trend from 2011 to 2012
#### Sales revenue seasonality was pronouced every 30 days (ACF plots), seasonality diminished if we extended over 90 days
#### Sales revenue did not have seasonality over a weekly duration
### Optimal RNN model for sales revenue forecasting
#### Look back period of 30 days
#### Model with first and second layer of 128 units and dense layer with 1 unit
#### Batch size of 64
### Optimal RNN model for sales volume (quantity) forecasting
#### Look back period of 30 days
#### Model with first and second layer of 32 units and dense layer with 1 unit
#### Batch size of 64


## Installation 

### The project in the repository will include the following files
#### Readme file: Readme.md
#### Jupyter Notebook: online_retail_model.ipynb
#### Data file: OnlineRetail.xslx

### Google Colabs -based 
#### Create a project directory and loading the Jupyter notebook
##### Create a Google Drive project directory
##### Upload the online_retail_model.ipynb file on to a Google Drive project directory


#### Data set up: 
##### Create the directory data/ under the Google Drive project directory
##### Upload the  OnlineRetail.xslx onto the data directory

### Local environment - based
### Create a project directory and loading the Jupyter notebook
#### Download online_retail_model.ipynb file on to the project directory
#### Upload file onto the Jupyter Notebook and open it

### Data set up: 
#### Create the directory data/ under the root directory of Jupypter Notebook
#### Save the OnlineRetail.xslx file under this directory

## Usage
#### After setting up the data, you can run the Python code in the Jupyter notebook 
#### Please note that if you are using Google Colabs - you need to provide permission to connect Google Drive and update the path
#### Please note that if you are using local environment - you will need to comment the section of the code where it is mounting the Google Drive
#### Please make sure the file path for the data file is updated
#### The code has markdown sections that outline the approach of the analysis and can help you understand the logic
#### Upon running the code, you will generate string outputs and plotly

## Data
### This data comes to us from UCI - data set contains 541909 sales transactions between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online global retail company. The company mainly sells unique all-occasion gifts to customers in 37+ countries, many of whom are wholesalers.
### The data contains the following
#### Details of bank customer
#### Invoice date
#### Stock code, quantity sold, price
#### Customer ID, Country

## Contribution
### You can extend and refine the model by exploring the following
#### Developing models with additional layers, with varying number of units per layer
#### Developing forecasting models for top SKUs
#### Developing forecasting models for UK and non UK shipments
#### Taking into special factors such as "holidays" for developing models 
 

