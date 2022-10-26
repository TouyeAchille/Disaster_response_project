# Disaster Response Project :

## Project Overview
In this project, we'll analyze disaster data from Appen (formally Figure 8) to build a model for an API that classifies disaster messages. In the Project, you'll find a data set containing real messages that were sent during disaster events. We will be creating a machine learning pipeline to categorize these events so that you can send the messages to an appropriate disaster relief agency. This project will include a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data. Below are a few screenshots of the web app.


## Project Components
We'll need to complete this three components for this project.

1. ETL Pipeline
In a Python script, process_data.py, write a data cleaning pipeline that:

Loads the messages and categories datasets
Merges the two datasets
Cleans the data
Stores it in a SQLite database

2. ML Pipeline
In a Python script, train_classifier.py, write a machine learning pipeline that:

Loads data from the SQLite database
Splits the dataset into training and test sets
Builds a text processing and machine learning pipeline
Trains and tunes a model using GridSearchCV
Outputs results on the test set
Exports the final model as a pickle file

3. Flask Web App & Deployed Heroku app online
build web app with boostrap library for front web app, flask for web backend and  Deployed Heroku app online

4. Repository layout
