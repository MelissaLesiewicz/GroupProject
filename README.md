

# Stroke Outcomes Prediction Model

For this project, our group is using a dataset related to patient stroke outcomes to train and compare several machine learning models to predict stroke outcomes based on input variables. We will train a variety of different model types, using several different data preprocessing techniques for each one and compare the accuracy and effectiveness of each model. The best performing ones will be selected for presentation on the project's dashboard including the ability to try out the models prediction with user generated input variables, as well as a presentation of some of the findings from the dataset in regards to stroke outcomes broken down by data categories.

The dataset contains a combination of medical data and non-medical lifestyle data. We intend to create a predictive model using the entire dataset, but also compare and contrast predictions when using only medical data, or only non-medical data, as well and identifying which data categories seem to be predictive that we would not have expected.

Of course, this model is not intended for any medical use, but merely high level analysis of the limited data we have available, to find if there are any interesting correlations for stroke outcomes within the data categories of this set.


## Data Used

Kaggle Stroke Prediction dataset: https://www.kaggle.com/fedesoriano/stroke-prediction-dataset
Sample of our dataset:
![Dataset Sample](https://user-images.githubusercontent.com/86027932/141658648-af4c5735-01f1-40b6-97e3-1f8d88a5c3f1.PNG)

## Technologies Used
### Data Cleaning and Analysis
Pandas will be used to clean the data, split the data (training and tsting) and Further data analysis will be completed using Python.

### Database Storage
Postgress SQL is the database we intend to use.
Database ERD:
![QuickDBD-export](https://user-images.githubusercontent.com/86027932/141658675-42095895-4ae5-43ff-af67-31071984344a.png)

### Machine Learning
SciKitLearn & Tensowflow are the ML library we'll be using to create a classifier. Our training and testing setup is over/undersampled to mitigate an umbalanced dataset.

### Dashboard
Tableau visuals and story telling functionality will be used to provide user interactivity and identified insights.

### Stretch Goal
Set up a webpage using Javascript forms to allow users to enter their medical, personal and lifestyle data to how likely the would be to have a stroke.

### Presentation
https://docs.google.com/presentation/d/1vC_XtYIOsB0pjBaotyLygCcyrjDMaYhZc4R6myExGRU/edit?usp=sharing
