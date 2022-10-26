# Disaster Response Project :

## Project Overview
In this project, we'll analyze disaster data from Appen (formally Figure 8) to build a model for an API that classifies disaster messages. In the Project, you'll find a data set containing real messages that were sent during disaster events. We will be creating a machine learning pipeline to categorize these events so that you can send the messages to an appropriate disaster relief agency. This project will include a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data. Below are a few screenshots of the web app.

## Project Components
We'll need to complete this three components for this project.

1. ETL Pipeline
In a Python script, process_data.py, write a data cleaning pipeline that:

- Loads the messages and categories datasets
- Merges the two datasets
- Cleans the data
- Stores it in a SQLite database

2. ML Pipeline
In a Python script, train_classifier.py, write a machine learning pipeline that:

- Loads data from the SQLite database
- Splits the dataset into training and test sets
- Builds a text processing and machine learning pipeline
- Trains and tunes a model using GridSearchCV
- Outputs results on the test set
- Exports the final model as a pickle file

3. Flask Web App & Deployed Heroku app online
- build web app with boostrap library for front, flask for backend and Deployed Heroku app online


├── ETL_pipeline_prep
│   ├── categories.csv
│   ├── ETL Pipeline Preparation.ipynb
│   └── messages.csv
│
├── ML_pipeline_prep
│   ├── best_model.sav
│   ├── DisasterResponse.db
│   ├── ML Pipeline Preparation.ipynb
│   └── model_est50_vocabnone_size33_rn42_idftrue_depth1.joblib

## Project Details
Below are additional details about each component :

Project Workspace - ETL :
The first part of this data pipeline is the Extract, Transform, and Load process. Here, we will read the dataset, clean the data, and then store it in a SQLite database. For this part We choose to clean data with pandas in order to load the data into an SQLite database by using pandas dataframe .to_sql() method, which you can use with an SQLAlchemy engine.

Project Workspace - ML Pipeline :
For the machine learning portion, we will split the data into a training set and a test set. Then, we will create a machine learning pipeline that uses NLTK, as well as scikit-learn's Pipeline and GridSearchCV to output a final model that uses the message column to predict classifications for 36 categories (multi-output classification). Finally, we will export our model to a pickle file. After completing the notebook, we include the final machine learning code in train_classifier.py.

Data Pipelines - python Scripts :
After we are complete our notebooks for the ETL and machine learning pipeline, we transfer all our work into Python scripts, process_data.py and train_classifier.py.

Flask App
In the last step, we'll display our results in a Flask web app

## Repository layout
The coding for this project can be completed using the Project Workspace IDE provided or Vscode. Here's the file structure of the project:

- Web_app
├── app  
│   │   
│   └── templates
│   │     ├── go.html
│   │     └── master.html   
│   └── routes.py
├── data
│   ├── disaster_categories.csv
│   ├── disaster_messages.csv
│   ├── DisasterResponse.db
│   └──process_data.py
│
├── models
│   ├── DisasterResponse_est50_vocabnone_size33_rn42.db
│   ├── DisasterResponse_est50_vocabnone_size33_rn42_idftrue_depth1.db
│   ├── model_est50_vocabnone_size33_rn42_idftrue_depth1.joblib
│   ├── model_est50_vocabnone_size33_rn42.joblib
│   └── train_classifier.py
│
├── LICENSE
├── README.md
├── requirement.txt
│
└── Disaster_response_app

  - app
|   - template
|   |- master.html  # main page of web app
|   |- go.html  # classification result page of web app
    |- run.py  # Flask file that runs app

- data
|- disaster_categories.csv  # data to process 
|- disaster_messages.csv  # data to process
|- process_data.py
|- DatabaseResponse.db   # database to save clean data to

- models
|- train_classifier.py
|- classifier.pkl  # saved model 

- README.md

