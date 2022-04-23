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
  - 4 Machine learning models implemented
    1) Artificial Neural Network
    2) Logistic Regression
    3) Random Forest
    4) XGBoost
  - Comparison of models with F1 score and Accurary
  - Findings: We found that Random Forest has the highest prediction accuracy (94.09%) and F1 score (96.95%)

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

# What we learnt in this project
- Additional methods of data visualisation:
  - 2 Dimensional KDE Plots - Effects of 2 different predictors on probability of response variable
  - Stacked bar charts with offset-y: Comparison between the 2 categories of response variable on a highly imbalanced dataset
- Concepts to handle highly imbalanced data (SMOTE)
- Concepts and implementation of 4 new machine learning models with their respective libraries required
  - Artificial Neural Network
  - Logistic Regression
  - Random Forest
  - XGBoost
- Concepts on Model Comparison (F1 Score, recall, area under ROC curve). In the case of imbalanced datasets, F1 Score is a better indicator of predictive power than prediction accuracy.

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

# Conclusion
|          | Logistic Regression | Random Forest | ANN  | XGBoost |
|----------|---------------------|---------------|------|---------|
| Accuracy |                0.93 |          0.94 | 0.81 |    0.93 |
| F1 Score |                0.96 |          0.97 | 0.89 |    0.96 |

# References
- [Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- [Research Paper 1](https://www.frontiersin.org/articles/10.3389/fneur.2021.734345/full)
- [Research Paper 2](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-019-0998-2)
- [EDA 1](https://towardsdatascience.com/step-by-step-exploratory-data-analysis-on-stroke-dataset-840aefea8739)
- [EDA 2](https://medium.com/geekculture/performing-exploratory-data-analysis-on-stroke-dataset-1b4885989030)
- [2D Density Plots](https://towardsdatascience.com/simple-example-of-2d-density-plots-in-python-83b83b934f67)
- [Composite Variables](https://study.com/academy/lesson/composite-variable-definition-lesson-quiz.html)
- [SMOTE 1](https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/)
- [SMOTE 2](https://datascience.stackexchange.com/questions/28227/why-will-the-accuracy-of-a-highly-unbalanced-dataset-reduce-after-oversampling)
- [F1-Score, Accuracy, ROC, AUC](https://neptune.ai/blog/f1-score-accuracy-roc-auc-pr-auc#:~:text=F1%20score%20vs%20Accuracy,-Both%20of%20those&text=Remember%20that%20the%20F1%20score,observations%20both%20positive%20and%20negative.)
- [XGBoost](https://books.google.com.sg/books?hl=en&lr=&id=HgmqDwAAQBAJ&oi=fnd&pg=PP1&dq=xgboost+python&ots=nMiCj5I6ND&sig=YzRWuFIwXjxOd0kvXtBAWSorqhg&redir_esc=y#v=onepage&q=xgboost%20python&f=false)
- [ANN](https://ieeexplore.ieee.org.remotexs.ntu.edu.sg/stamp/stamp.jsp?tp=&arnumber=8079581)
- [Random Forest](https://www.nature.com.remotexs.ntu.edu.sg/articles/s41598-021-89434-7)
- [Logistic Regression](https://medium.com/@timilearns_65018/a-logistic-regression-model-to-predict-stroke-occurrence-with-an-imbalanced-dataset-ii-1aa5b800a580)
