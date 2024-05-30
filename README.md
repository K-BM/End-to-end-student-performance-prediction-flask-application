# Student Math Score Prediction Application

## Overview

This repository contains an end-to-end application implemented with Flask, designed to predict the math scores of students based on several input attributes. The application involves data ingestion, preprocessing, model training, and prediction. The best performing model is selected based on the highest R² score and is stored for making predictions through the Flask web interface.

## Features

- Data Ingestion: Collect and preprocess training and test data.
- Model Training: Train multiple regression models and select the best one.
- Model Storage: Save the best model and preprocessing steps as pickle files.
- Prediction: Load the best model and preprocessing steps to make predictions.
- Web Interface: Interact with the application through a user-friendly web interface.

## Directory Structure

.
├── .git
│   ├── COMMIT_EDITMSG
│   ├── config
│   ├── description
│   ├── HEAD
│   ├── hooks
│   ├── index
│   ├── info
│   ├── logs
│   ├── objects
│   ├── refs
│   └── .gitignore
├── app.py
├── artifacts
│   ├── data.csv
│   ├── model.pkl
│   ├── preprocessor.pkl
│   ├── test.csv
│   ├── train.csv
│   └── __init__.py
├── logs
├── notebook
│   ├── 1 . EDA STUDENT PERFORMANCE .ipynb
│   └── 2. MODEL TRAINING.ipynb
├── README.md
├── requirements.txt
├── setup.py
├── src
│   ├── components
│   ├── exception.py
│   ├── logger.py
│   ├── pipeline
│   ├── utils.py
│   └── __init__.py
└── templates
    ├── home.html
    └── index.html

## Setup Instructions

    Clone the Repository:

        git clone https://github.com/K-BM/End-to-end-student-performance-prediction-flask-application.git
        cd student-math-score-prediction

## Install Dependencies:

pip install -r requirements.txt

## Run Data Ingestion and Model Training:
python src/components/data_ingestion.py

## Launch the Flask Application:

    python app.py

## Usage

    Data Ingestion and Model Training:
        The script data_ingestion.py will handle the collection and preprocessing of training and test data. It will train multiple models and store the best model along with preprocessing steps in pickle files.

    Running the Flask Application:
        Start the Flask server using app.py. Open your web browser and navigate to http://127.0.0.1:5000/predict_score to interact with the application.

    User Interaction:
        The web interface consists of two pages: index.html and home.html.
        index.html serves as the landing page.
        home.html allows users to input student attributes and make predictions on their math scores.

## Components

    data_ingestion.py:
        Collects and processes the training and test data.
        Trains multiple regression models.
        Selects and saves the best model based on the highest R² score.

    model_training.py:
        (Optional) Additional module to handle model training separately.

    prediction.py:
        Loads the preprocessed data and the best model.
        Makes predictions based on user input through the Flask app.

    Flask App (app.py):
        Sets up the Flask web server.
        Routes user requests and renders the web pages.
        Handles user input and invokes the prediction pipeline.

## File Descriptions

    src/components/data_ingestion.py: Handles data ingestion, processing, and model training.
    src/components/model_training.py: Contains functions for training models (optional).
    src/components/prediction.py: Manages loading the model and making predictions.
    templates/index.html: The landing page of the application.
    templates/home.html: The page for inputting student attributes and displaying predictions.
    app.py: The main Flask application file.