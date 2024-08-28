# Misinfonix
## **Overview**
---
The Aim of this project is to use the Natural Language Processing and Machine learning to detect misinformation based on the text content of the Article. And after building the suitable Machine learning model to detect the fake/true information then to deploye it into a web interface using laravel.

## **Dataset**
---
All of the Dataset that used are availabe in public Domain. Most of the Dataset are collected from Kaggle (https://www.kaggle.com/)
different datsets contain different column and different information like [title,text,subject,news_url,author]

For model Build need only text and Label, The final dataset will contain only 2 column ['Article','Lable']
  * For text we will create a content column named 'Article' which is the Combination Header and text
  * In the Lable column 
      * 1 represent true
      * 0 represent fake

## **Data preprocessing**
---
1. Remove all unwanted columns.
2. Remove All Missing Values Records.
3. Removing all the extra information like brackets, any kind of puctuations - commas, apostrophes, quotes, question marks from Text.
4. Remove all the numeric text, urls from Text.

## **ML model Traning and Building**
---
We have used Logistic Regression, Stochastic Gradient Descent, DecisionTree, Multinomial Naive Bayes and Bernoulli Naive Bayes classifiers.

## **Running Project Locally**
---
Just type the following on terminal:
php artisan serve


## **Folders and Files Use**
---

resources/views/
  - This directory contains view files in a Laravel application. These files are responsible for presenting the user interface to the end-user. Examples of view files commonly found here include blade templates (.blade.php) that define the structure and layout of web pages.

app/Http/Controllers/
  - In Laravel, controllers handle the application logic, process incoming requests, and return responses. Here's what each file likely does:
    - SocialController.php : This controller is responsible for handling the login functionality for various social media platforms such as Google, Facebook, etc. It contains methods for authenticating users through these platforms and managing user sessions.
    - ReportController.php : This controller deals with generating and managing reports within the application. Additionally, it's responsible for sending reports to the specified email address (factcheck@rappler.com). This controller may include methods for generating reports based on user input or system events and handling the emailing process.
    - PythonController.php : Responsible for running the main Python script (app.py) located in the python/ directory from within the Laravel application. This controller likely handles the integration between the Laravel framework and the Python script.

python/
  - This directory appears to contain Python-related files and scripts used within the Laravel application:
    - app.py     : The main Python script that is executed by the PythonController.php. It likely serves a specific functionality within the Laravel application, such as text prediction or other machine learning tasks.
    - model.pkl  : Contains a trained machine learning model serialized using pickle, likely used within the Laravel application for making predictions based on the trained model.
    - ModelBuilding.ipynb : Jupyter Notebook file used for building machine learning models, containing code and explanations for various machine learning algorithms used in the application.

python/Datasets/
  - Contains different datasets in CSV format used for training and testing the machine learning model within the Laravel application.

python/url/
  - This directory contains Python scripts related to handling URLs, possibly for web scraping or fetching data from web pages:
    - Runner.py : Used when the input provided to the Laravel application is a URL, performing actions or processing based on the URL provided.
    - Scrape.py : Used for web scraping, extracting data from web pages, and possibly gathering information from external sources within the Laravel application.

