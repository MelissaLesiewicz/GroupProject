### GitHub structure
#### Home


***files:**
- *Hypothesis_Test.ipynb*: Hypothesis T-Test.
- *Project Report.docx*: Word document describing the project.
- *Stroke Prediction Dashboard PDF.pdf*: pdf copy of our Tableau Story Telling Dashboard.
- *Stroke Prediction Project.twbx*: Copy of our Tableau public Dashboad.
- *Chosen_MachineLearning_model_optimized.ipynb*: Selected model optimization: sklearn pipeline and GridSearchCV.
- *User_Stroke_Prediction_ML_model.ipynb*: Python script to enter your data and predict your stroke likelihood.

***folders:**
- *DataProcessing*: Data preprocessing script to explore, clean and insert data into AWS PostgreSQL database.
- *DataSampling*: Data sampling techniques utilized for Machine Learning models.
- *Database*: Entity Relationship Diagram files.
- *EDA*: Exploratory Data Analysis.
- *Images*: Readme, reports and presentation images.
- *Machine_Learning_Models*: Training, Testing and assessment of all the ML models generated for this project.
- *Resources*: All dataset imported and generated for EDA, Sampling and Machine Learning models.

# Stroke Outcomes Prediction Model

For this project, our group is using a dataset related to patient stroke outcomes to train and compare several machine learning models to predict stroke outcomes based on input variables. We will train a variety of different model types, using several different data preprocessing techniques for each one and compare the accuracy and effectiveness of each model. The best performing ones will be selected for presentation on the project's dashboard including the ability to try out the models prediction with user generated input variables, as well as a presentation of some of the findings from the dataset in regards to stroke outcomes broken down by data categories.

The dataset contains a combination of medical data and non-medical lifestyle data. We intend to create a predictive model using the entire dataset, but also compare and contrast predictions when using only medical data, or only non-medical data, as well and identifying which data categories seem to be predictive that we would not have expected.

Of course, this model is not intended for any medical use, but merely high level analysis of the limited data we have available, to find if there are any interesting correlations for stroke outcomes within the data categories of this set.

## Hypothesis

- How do the non-medical factors impact our model’s accuracy, precision, and recall?
Is a high average blood glucose level a good indicator of stroke risk?

- *Null hypothesis(Ho)*: High average blood glucose levels do not indicate stroke outcomes.
- *Alternate Hypothesis(Ha)*: Patients with high average blood glucose levels are more likely to suffer a stroke.

### T-Test results

**pvalue=2.872279057752545e-21 rejects Ho** hence patients with high average blood glucose are likely to suffer a stroke


script reference: https://github.com/MelissaLesiewicz/GroupProject/blob/main/Hypothesis_Test.ipynb

## Our winning model 
classifier: Logistic Regression
**performance:**
- Accuracy: 0.87
- F1 Scores: 0.87/0.87
- Area under the curve (AuC): 0.9364

![Logistic Refression Stats](https://github.com/MelissaLesiewicz/GroupProject/blob/main/Images/LogisticRegression_AUC_0.93.png)


## Stretch Goal
Allow users to enter their medical, personal and lifestyle data to how likely the would be to have a stroke.

### Python script 

User input for stroke prediction:

![User Input](https://github.com/MelissaLesiewicz/GroupProject/blob/main/Images/ML_model_UserInput.png)

Output:

- **Very likely to have a stroke**
or
- Unlikely to have a stroke


script reference: https://github.com/MelissaLesiewicz/GroupProject/blob/main/User_Stroke_Prediction_ML_model.ipynb


# Communication
Initial team meeting via Zoom. Discussued project requirements and assigned individual responsibilities.
Weekly team meetings via Zoom occur twice per week during our scheduled class time.
Team communication via Slack as needed to update team members of progress and to ask for assistance.

# Data Used

Kaggle Stroke Prediction dataset: https://www.kaggle.com/fedesoriano/stroke-prediction-dataset
Sample of our dataset:
![Dataset Sample](https://user-images.githubusercontent.com/86027932/141658648-af4c5735-01f1-40b6-97e3-1f8d88a5c3f1.PNG)

# Technologies Used

## Data Cleaning and Analysis
Pandas will be used to clean the data, split the data (training and tsting) and Further data analysis will be completed using Python.

- Exploratory Data Analysis: pandas, matplotlib, seaborn

## Database Storage

Database ERD:
![QuickDBD-export](https://user-images.githubusercontent.com/86027932/141658675-42095895-4ae5-43ff-af67-31071984344a.png)

SQL script: https://github.com/MelissaLesiewicz/GroupProject/blob/main/Database/ERD_DB_creation.sql

**Tools:**
- Database Enginge:PostgreSQL 12.8 and pgAdmin 4 
- Hosted in Amazon Web Services (AWS)
- Python libraries & drivers: sqlalchemy and psycopg2

## Machine Learning
SciKitLearn & Tensowflow are the ML library we'll be using to create a classifier. Our training and testing setup is over/undersampled to mitigate an umbalanced dataset.

- ML models: numpy, sklearn and tensorflow 
- Save persisten objects (models, scalers): joblib

## Dashboard
Tableau visuals and story telling functionality will be used to provide user interactivity and identified insights.

- Tableau public: https://public.tableau.com/shared/KFC9TY33W?:display_count=n&:origin=viz_share_link

![Stroke Story Telling](https://github.com/MelissaLesiewicz/GroupProject/blob/main/Images/Tableau_Dashboard.png)



# Presentation
https://docs.google.com/presentation/d/1vC_XtYIOsB0pjBaotyLygCcyrjDMaYhZc4R6myExGRU/edit?usp=sharing
