## SC1015 DSAI Project Stroke Prediction BCF1 Group 7

<img width="960" alt="image" src="https://user-images.githubusercontent.com/34325457/164873887-e5723976-93e8-411b-b5b0-02aa45c97c2e.png">

# Objective
Singapore has an ageing population, and the incidence of stroke has been rising consistently. If we can predict a stroke before it happens, many fatal accidents can be prevented. However, traditional stroke prediction models often rely on medical data that is unattainable by a typical individual, so the prediction process can be very cumbersome. What if there is a way to utilise easily accessible data like marriage status, bmi, age, gender, work type... for stroke prediction? If successful, then perhaps we could look into exploring other indirect factors to build even simpler stroke prediction models that the general public can use even without medical knowledge and extensive personal medical data!

# Dataset Folder
- healthcare-dataset-stroke-data.csv - Original CSV file
- stroke_cat.csv - Preprocessed data

| Column            | Description |
|-------------------|-------------|
| id                | ID |
| gender            | Male / Female |
| age               | Age |
| hypertension      | 1 / 0
| heart_disease     | 1 / 0
| ever_married	    | Yes / No
| work_type	        | Private sector / Government Job / Self-employed / Never worked / Children |
| Residence_type	  | Rural / Urban |
| avg_glucose_level	| Average glucose level |
| bmi	              | (weight / height) ^ 2 |
| smoking_status	  | Never smoked / Formerly smoked / Smokes / Unknown |
| stroke (Label)    | 1 / 0 |

# Notebooks Folder
- Exploratory_Data_Analysis_&_Data_Preprocessing.ipynb
  - EDA
  - Fill missing BMI values with mean BMI
  - One-hot encoding

- Machine_Learning_Models.ipynb
  - SMOTE
  - 4 Machine learning models
     1) Artificial Neural Network
     2) Logistic Regression
     3) Random Forest
     4) XGBoost
  - Comparison of models with F1 score and Accurary, we found that Random Forest has the highest prediction accuracy (94.09%) and F1 score (96.95%)

# Libraries
- os
- numpy
- pandas
- scipy
- seaborn
- matplotlib
- keras
- xgboost
- sklearn
- imblearn
- tensorflow

# Directions
1) Import *Exploratory_Data_Analysis_&_Data_Preprocessing.ipynb* to Google Colab and run the whole notebook
2) At the end, proprocessed data will be saved as *stroke_cat.csv*
3) Download *stroke_cat.csv* and upload it to Google Drive before running *Machine_Learning_Models.ipynb*

<kbd><img width="541" alt="image" src="https://user-images.githubusercontent.com/34325457/164873830-06b49757-8b48-4ceb-b0dc-a194a58b6c78.png"></kbd>

<kbd><img width="541" alt="image" src="https://user-images.githubusercontent.com/34325457/164873802-7b419359-0c5f-47a5-baf3-cdbc60c9c9ff.png"></kbd>


# Indivual Contributions
- Si Ming Zhou
  - EDA
  - Logistic Regression
  - Slides and Presentation

- Jeremy Lim
  - Random Forest
  - Slides and Presentation

- Siah Wee Hung
  - EDA
  - ANN and XGBoost Models

# References
