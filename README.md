# Disaster Response Classification Pipeline

## Project Motivation and Description
This project leverages a dataset provided by [Appen](https://www.appen.com/), containing tens of thousands of real messages from various sources during disaster events. We have constructed a powerful **multi-label classification machine learning (ML) model** aimed at efficiently categorizing messages sent during disasters. The dataset encompasses information across 36 predefined categories, including but not limited to aid-related, medical assistance, search and rescue, among others. By effectively categorizing these messages, we are able to swiftly relay them to the appropriate disaster relief organizations, thereby enhancing their information processing efficiency and enabling targeted and timely rescue efforts.

Within the project, we have established a comprehensive technical framework, encompassing **ETL** (Extract, Transform, Load), **NLP** (Natural Language Processing), and **ML pipelines**, all implemented using the **SQLite database** and **Python** programming language. Given that disaster-related information can fall into multiple categories, we are dealing with a multi-label classification task. This implies that a single message can belong to one or more categories simultaneously.

Ultimately, we have utilized **Flask** and **Plotly** technologies to create an intuitive web application for showcasing the visualization of data. This application allows stakeholders to easily input information and instantly obtain classification results. Below is a screenshot of the web application, showcasing the user interface and visual representation of classification outcomes:

![Screenshot of Web App](https://github.com/Ting-DS/Disaster_Response_Classification_Pipeline/blob/main/Web_App.png)

## File Description
~~~~~~~
        disaster_response_pipeline
          |-- app
                |-- templates
                        |-- go.html
                        |-- master.html
                |-- run.py
          |-- data
                |-- disaster_message.csv
                |-- disaster_categories.csv
                |-- DisasterResponse.db
                |-- process_data.py
          |-- models
                |-- classifier.pkl
                |-- train_classifier.py
          |-- Preparation
                |-- categories.csv
                |-- ETL Pipeline Preparation.ipynb
                |-- ETL_Preparation.db
                |-- messages.csv
                |-- ML Pipeline Preparation.ipynb
                |-- README
          |-- README
~~~~~~~
## Installation
Must runing with Python 3 with libraries of numpy, pandas, sqlalchemy, re, NLTK, pickle, Sklearn, plotly and flask libraries.

## File Descriptions
1. App folder including the templates folder and "run.py" for the web application
2. Data folder containing "DisasterResponse.db", "disaster_categories.csv", "disaster_messages.csv" and "process_data.py" for data cleaning and transfering.
3. Models folder including "classifier.pkl" and "train_classifier.py" for the Machine Learning model.
4. README file
5. Preparation folder containing 6 different files, which were used for the project building. (Please note: this folder is not necessary for this project to run.)

## Instructions
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

## Licensing, Authors, Acknowledgements
Many thanks to Figure-8 for making this available to Udacity for training purposes. Special thanks to udacity for the training. Feel free to utilize the contents of this while citing me, udacity, and/or figure-8 accordingly.

### NOTICE: Preparation folder is not necessary for this project to run.
# Disaster_Response_Classification_Pipeline
