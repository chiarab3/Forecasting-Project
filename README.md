# Forecasting-Project

This repository contains the code and documentation for a project that predicts snowfall based on historical weather data.
Two machine learning models – **Random Forest** and **XGBoost** – were used to address a time-shifted binary classification problem:  
> Will it snow tomorrow, 20 years ago?

If today is April 1, 2025, the goal is to forecast the weather for April 2, 2005.

## Dataset

The dataset includes climate observations from over 9,000 weather stations around the world. Each row contains temperature, humidity, wind speed, and other meteorological data, along with a binary label indicating if it snowed the next day.

## Environment Setup

This project was developed in a Conda environment running on WSL (Ubuntu 22.04).

```bash
#Create and activate the environment
conda create -n forecasting python=3.8
conda activate forecasting

#Install required packages
pip install -r requirements.txt

#Authenticate with GCP
gcloud auth application-default login

#Set your default project
gcloud config set project [YOUR_PROJECT_ID]
```

## How to Run
Once your environment is set up, launch the Jupyter Notebook:
```bash
jupyter notebook forecasting_project.ipynb
```
Then execute the cells step-by-step to train, evaluate, and interpret the models.

## Repository
- `forecasting_project.ipynb` is the ML pipeline
- `final_df.csv` is the cleaned dataset used for modeling
- `requirements.txt` contains the project dependencies 

