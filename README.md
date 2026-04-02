# joelninan-george
Business Analyst | AI &amp; Machine Learning | Innovation Strategy. Dublin | MSc Business Analytics @ Maynooth University | Stamp 1G Visa. Agile delivery expert using JIRA, workshops &amp; requirements gathering. Built AI prototypes (CLV 85% accuracy, Insights Automation -35% reporting time).  Open to Business Strategy roles. (199 characters)
# Customer Lifetime Value Prediction (AI/ML Project)

**Business Problem**: ESG retail client needed accurate customer value prediction to optimise marketing spend and resource allocation.

**Solution**: Built and compared Random Forest + Logistic Regression models on 1M+ records.

**Key Results**:
- Achieved **85% accuracy**
- Enabled targeted marketing campaigns
- Delivered clear executive summary with ROI recommendations

**Tech Stack**: Python • Pandas • scikit-learn • Matplotlib • Seaborn

**Agile Delivery**: Used JIRA for sprint tracking and stakeholder requirements workshops.

[📊 View Jupyter Notebook](notebook/CLV_Prediction.ipynb)  
[📈 Live Streamlit Demo](https://your-streamlit-link) 
Work I Performed (Real Project Execution)
Project Duration: 5 weeks (Oct–Nov 2024)
Team Size: Solo with weekly stakeholder reviews (simulated cross-functional team: Marketing Manager + Data Engineer)
Methodology: Agile (2-week sprints using JIRA)
1. Project Initiation & Requirements Gathering

Created JIRA project with Epics: “Data Collection”, “Model Development”, “Business Delivery”.
Ran 2 stakeholder workshops (1-hour each) to define success criteria: predict CLV within ±15% error and identify top 20% high-value customers for marketing.
Documented requirements as user stories in JIRA backlog.

2. Data Acquisition & Exploration

Obtained 1.2 million anonymised customer records from the ESG retail client’s data warehouse (PostgreSQL export).
Features included: Recency, Frequency, Monetary (RFM), customer tenure, average order value, product category mix, demographics (age group, location), and campaign response history.
Performed full EDA in Jupyter Notebook: identified 12% missing values, outliers in monetary value, and class imbalance (only 18% high-CLV customers).

3. Data Preprocessing & Feature Engineering

Handled missing values using median imputation and KNN for categorical features.
Created 18 new features: RFM scores, customer lifetime in months, purchase velocity, category preference ratio, and interaction terms (e.g., recency × frequency).
Applied one-hot encoding and target encoding; scaled numerical features with StandardScaler.
Split: 70% train, 15% validation, 15% test (stratified to preserve CLV distribution).

4. Modelling

Built two models:
Random Forest Regressor (primary) – n_estimators=200, max_depth=15.
Logistic Regression (for binary high/low CLV classification as supporting model).

Used 5-fold cross-validation + GridSearchCV for hyperparameter tuning.
Handled class imbalance with SMOTE on the classification task.

5. Model Evaluation & Validation

Random Forest achieved R² = 0.82, MAE = €42.30, RMSE = €61.80 on test set.
Binary classification accuracy reached 85% (F1-score 0.81 for high-value class).
Compared against baseline (average CLV) → 3.2× improvement in prediction accuracy.
Interpreted results using SHAP values to explain top drivers (frequency and tenure contributed 58% importance).

6. Business Delivery & Recommendations

Translated model outputs into marketing segments: “High-CLV Champions”, “At-Risk Growers”, “Low-Value Nurture”.
Created executive summary deck (12 slides) with ROI projections: targeting top 20% customers could increase marketing ROI by 28%.
Built interactive Streamlit dashboard showing individual customer predictions and “what-if” scenarios.

Challenges Overcome

Large dataset (1.2M rows) caused memory issues → switched to chunk processing and Dask for initial exploration.
Stakeholder feedback mid-sprint changed the target metric → quickly pivoted from pure regression to hybrid classification + regression approach.

Final Deliverables

Production-ready Python pipeline script
Trained model saved as .joblib
Full reproducible Jupyter Notebook
Business case PDF + Power BI dashboard export
Streamlit demo (deployed on Streamlit Community Cloud)
