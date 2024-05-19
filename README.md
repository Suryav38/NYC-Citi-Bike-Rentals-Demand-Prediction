# NYC Citi Bike Rentals Demand Prediction Model

## Overview
This project aims to develop a deep learning model to classify the daily demand for Citi Bikes in Jersey City, NY, into three categories: High, Medium, and Low. The model's primary objective is to optimize bike distribution, increase resource utilization, enhance operational efficiency, and improve customer satisfaction by reducing potential wait times.

## Table of Contents
- [Project Structure](#project-structure)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Model Development](#model-development)
- [Feature Importance](#feature-importance)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [Business Value](#business-value)
- [Authors](#authors)

## Project Structure
The project consists of the following files:
- `Data Extraction.ipynb`: Notebook for extracting and loading data.
- `Data_Exploration.ipynb`: Notebook for performing exploratory data analysis.
- `Feature Importance by permutation.ipynb`: Notebook for evaluating feature importance.
- `Model.ipynb`: Notebook for developing and training the deep learning model.
- `IE434_Presentation.pdf`: Final project presentation.
- `README.md`: Project documentation.

## Problem Statement
The project aims to classify daily demand for Citi Bikes into three categories:
- **High Demand**
- **Medium Demand**
- **Low Demand**

### Objectives
- Optimize bike distribution to meet customer demand efficiently.
- Increase resource utilization and operational efficiency.
- Enhance customer satisfaction by reducing potential wait times.

## Dataset
The dataset includes:
- **Bike Rental Data**: From January 2022 to September 2023 for Jersey City, NY.
- **Weather Data**: Daily climate data for the same period.

### Columns in Bike Rental Data:
- `Ride ID`: Unique identifier for each ride.
- `Rideable Type`: Type of bike used.
- `Started At`: Start date and time of the ride.
- `Ended At`: End date and time of the ride.
- `Start Station Name`: Name of the start station.
- `Start Station ID`: Unique identifier for start station.
- `End Station Name`: Name of the end station.
- `End Station ID`: Unique identifier for end station.
- `Start Latitude`: Latitude of the start location.
- `Start Longitude`: Longitude of the start location.
- `End Latitude`: Latitude of the end location.
- `End Longitude`: Longitude of the end location.
- `Member or Casual`: Type of rider.

### Columns in Weather Data:
- `Date`: Date.
- `PRCP`: Precipitation value for the day.
- `SNOW`: Snowfall.
- `TMAX`: Maximum temperature of the day.
- `TMIN`: Minimum temperature of the day.

## Data Preprocessing
- Dropped missing values.
- Scaled latitude and longitude values.
- Converted the numerical demand variable into categorical variable (High, Medium, Low).

## Exploratory Data Analysis
- Analyzed rental patterns to uncover seasonal and weekly demand fluctuations.
- Investigated ride durations, time intervals, and user types.
- Identified distinct usage trends between members and casual riders.

## Model Development
### Baseline Model
- **Model**: Logistic Regression (Multinomial)
- **Accuracy**: 60.75%

### Deep Learning Model
- **Model**: GRU (Gated Recurrent Unit) based Recurrent Neural Network
- **Architecture**:
  - GRU Layer: Handles time-series predictions.
  - Dropout Layer: Reduces overfitting.
  - Linear Layer: Maps GRU output to desired output.
- **Best Model Configuration**:
  - Optimizer: Adam
  - Learning Rate: 0.001
  - Epochs: 600
  - Batch Size: 64
- **Accuracy**: 77.3%

## Feature Importance
Evaluated feature importance using permutation method:
- **Important Features**:
  - Longitude of Starting Point
  - Latitude of Starting Point
  - Minimum Temperature
  - Maximum Temperature

## Results
- Successfully developed a model to classify daily demand for Citi Bikes.
- Best model achieved an accuracy of 77.3%.

## Future Improvements
- Explore the use of Graph Neural Networks (GNNs) to integrate spatial data more effectively.

## Business Value
- **Optimized Fleet Management**: Efficiently manage bike distribution.
- **Maintenance and Staffing Schedules**: Plan better for high and low demand periods.
- **Dynamic Pricing Strategy**: Implement pricing strategies based on demand predictions.


