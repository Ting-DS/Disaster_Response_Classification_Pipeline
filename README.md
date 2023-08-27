# Disaster Response Classification Pipeline

## Project Motivation and Description
This project leverages a dataset provided by [Appen](https://www.appen.com/), containing tens of thousands of real messages from various sources during disaster events. We have constructed a powerful **multi-label classification machine learning (ML) model** aimed at efficiently categorizing messages sent during disasters. The dataset encompasses information across 36 predefined categories, including but not limited to aid-related, medical assistance, search and rescue, among others. By effectively categorizing these messages, we are able to swiftly relay them to the appropriate disaster relief organizations, thereby enhancing their information processing efficiency and enabling targeted and timely rescue efforts.

Within the project, we have established a comprehensive technical framework, encompassing **ETL** (Extract, Transform, Load), **NLP** (Natural Language Processing), and **ML pipelines**, all implemented using the **SQLite database** and **Python** programming language. Given that disaster-related information can fall into multiple categories, we are dealing with a multi-label classification task. This implies that a single message can belong to one or more categories simultaneously.

Ultimately, we have utilized **Flask** and **Plotly** technologies to create an intuitive web application for showcasing the visualization of data. This application allows stakeholders to easily input information and instantly obtain classification results. Below is a screenshot of the web application, showcasing the user interface and visual representation of classification outcomes:

![Screenshot of Web App](https://github.com/Ting-DS/Disaster_Response_Classification_Pipeline/blob/main/Web_App.png)

## Installation
To ensure proper functionality, it is required to run this project using Python 3 along with the following libraries:

- **numpy**
- **pandas**
- **sqlalchemy**
- **re**
- **NLTK**
- **pickle**
- **Sklearn**
- **plotly**
- **flask**

Please ensure that you have these libraries installed before proceeding with the project setup.

You can install these libraries using the following command:
```bash
pip install numpy pandas sqlalchemy nltk scikit-learn plotly flask
```

## File Description
~~~~~~~
        Disaster_Response_Classification_Pipeline
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

## File Descriptions

1. **App Folder**: This folder includes the "run.py" script and the "templates" folder for the web application.

2. **Data Folder**: Inside this folder, you will find the "DisasterResponse.db" SQLite database file, along with "disaster_categories.csv" and "disaster_messages.csv" datasets. The "process_data.py" script is also included for data cleaning and transfer.

3. **Models Folder**: This folder contains the trained machine learning model "classifier.pkl" and the "train_classifier.py" script used for model training.

4. **README File**: This file provides an overview of the project, its structure, and instructions for setup and usage.

5. **Preparation Folder**: This folder contains various files that were used during the project's development. **Please note that this folder is not necessary for the project's operation and can be disregarded**.

## Instructions
To properly set up your database and model for this project, follow these steps in the project's root directory:

1. Run the following commands:

    - To execute the ETL pipeline for data cleaning and database storage:
      ```
      python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
      ```

    - To run the ML pipeline for training the classifier and saving the model:
      ```
      python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
      ```

2. After completing the above steps, navigate to the app's directory and run the following command to launch the web app:
   ```
   python run.py
   ```

3. Open your web browser and visit the following URL:
   ```
   http://0.0.0.0:3001/
   ```
   
## Licensing, Authors, Acknowledgements
Many thanks to Figure-8 for making this available to Udacity for training purposes. Special thanks to udacity for the training. Feel free to utilize the contents of this while citing me, udacity, and/or figure-8 accordingly.

### NOTICE: Preparation folder is not necessary for this project to run.
# Disaster_Response_Classification_Pipeline
