# **Ted Talks views Prediction**

This project is the second capstone project we've done in our [Almabetter](https://almabetter.com) Data science curriculam. All the models we have developed in this project will be heavily based on regression since we have to predict a continuous dependent variable, which in this case is **views** of a video.

## **Introduction**

[TED](https://www.ted.com) stands for Technology, Entertainment and Design.

A TED talk refers to a recorded public-speaking presentation that was originally given at the main TED (technology, entertainment and design) annual event or one of its many satellite events around the world. TED is a nonprofit devoted to spreading ideas, usually in the form of short, powerful talks, often called "TED talks." These could be a motivational video, awareness, technical, Science entertainment, or any other genre.

TED is devoted to spreading powerful ideas on just about any topic. Founded in 1984 by Richard Salman as a nonprofit organization that aimed at bringing experts from the fields of Technology, Entertainment, and Design together, TED Conferences have gone on to become the Mecca of ideas from virtually all walks of life. As of 2015, TED and its sister TEDx chapters have published more than 2000 talks for free consumption by the masses and its speaker list boasts of the likes of Al Gore, Jimmy Wales, Shahrukh Khan, and Bill Gates.

## **Objective**
The main objective is to build a predictive model, which could help in predicting the views of the videos uploaded on the TEDx website.

## **Data Gathering and description**

The dataset is available at [kaggle](https://www.kaggle.com/code/dochev/predicting-ted-talks-views-with-ml-models/data).

**This Dataset consists of following Attributes**:

* talk_id : Talk identification number provided by TED

* title : Title of the talk

* speaker_1 : First speaker in TED's speaker list

* speakers : Speakers in the talk

* occupations : Occupations of the speakers

* about_speakers : Blurb about each speaker

* views(Dependent Variable) : Count of views

* recorded_date : Date the talk was recorded

* published_date : Date the talk was published to TED.com

* event : Event or medium in which the talk was given

* native_lang : Language the talk was given in

* available_lang : All available languages (lang_code) for a talk

* comments : Count of comments

* duration : Duration in seconds

* topics : Related tags or topics for the talk

* related_talks : Related talks (key='talk_id', value='title')

* url URL of the talk

* description : Description of the talk

* transcript : Full transcript of the talk

## **Python Libraries used**

**Datawrangling and manipulation:** 
* Numpy
* Pandas

**Visualization:** 
* Matplotib
* Seaborn 
* graphviz

**Machine learning Models:**
* Scikit-Learn

**Others:**
* datetime
* warnings

## **Models**

In this project we are implementing 7 machine learning algorithms to predict the target variable and then we'll apply optimization techniques on the one that gives best resulting accuracy out of all.

**Following algorithms have been used for predictions:-**

* Linear Regression
* Lasso Regression
* Ridge Regression
* Elastic Net Regression
* Decision Tree
* Random Forest Regression
* XGB Regression

## **Notable Findings**

* We were able to see that the linear algorithms were not performing optimally even with Gradient Boosting optimization, and the tree-based algorithms performed significantly better. This might be the result of data being less correlated linearly, with the target variable. But tree based algorithms were able to find other indirect relationships over the features and hence giving better results.

* Out of the tree-based algorithms, the Random Forest Regressor was providing an optimal solution towards achieving our Objective. We were able to achieve an R2 score of 0.99 in the train split, and 0.93 in the test split. We also noticed that even in the case of Decision tree, we were able to achieve an R2 score of 0.91 in the test split. This puts weight to the statement that tree based algorithms are significantly better compared to Linear models in this case.

* Once we found the best model to work with, We then implemented Grid Search Cross Validation (on Random Forest Regressor), to further optimize the model, and were able to achieve an R2 score of 0.99 in the train split, and 0.94 (at best it gave 0.96) in the test split.

* Finally, we conclude Random Forest with GridSearchCV to be the best model to achieve our objective. Also in future we can try implementing some other optimising techniques (say hyperparameter tuning, Bayesian Optimization, etc) to wind up with better results.

## **Contributors**

|Name(Github)    |  Email   | 
|---------|-----------------|
|[Arvind Krishna](https://github.com/Arvind-krishna) |     killerdude.arvind@gmail.com    |
|[Keshav Sharma](https://github.com/Keshav1506) |    keshav1506sharma@gmail.com    |
|[Jayesh Panchal](https://github.com/Jayesh-Panchal) |     jaypan290497@gmail.com    |
|[Sahil Ahuja](https://github.com/saahilahujaa) |     s.ahuja38@gmail.com    |
