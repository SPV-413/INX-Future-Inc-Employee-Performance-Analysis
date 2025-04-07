# INX Future Inc Employee Performance Analysis
## **Project Summary** 
INX Future Inc. has observed a decline in employee performance, leading to increased escalations and an 8% drop in client satisfaction. To address this, a data science project was initiated to analyze employee performance, identify key influencing factors, and provide recommendations for improvement.

---
## **Requirement**
The data for this project was provided by **IABAC™** and is based on **INX Future Inc.** (referred to as INX). INX is a leading data analytics and automation solutions provider with over 15 years of global presence and has been consistently rated among the top 20 best employers over the past 5 years.

*Note: The data is not sourced from a real organization.*  

The entire project was conducted in **Jupyter Notebook** using the **Python** programming platform.

---
## **Analysis**
### i) **Dataset Overview**
- **Source**: INX_Future_Inc_Employee_Performance_CDS_Project2_Data_V1.8.csv
- **Rows**: 1200
- **Columns**: 28 (including the target variable)
- **Target Variable**:
  - **PerformanceRating** represent an employee's performance rating within the organization.
    - 2 - Employee not performed well
    - 3 - Employee moderately performed 
    - 4 - Employee performs well
- **Features**:
  - **EmpNumber** shows unique ID number of each Employee and it is not required for modeling and analysing.
  - **Age** shows how much the employee is older.
  - **Gender** is the sex of employee (Male , Female).
  - **EducationBackground** is the specialization of employees in which they studied.
  - **MaritalStatus** shows that the employee is married or not (Married, Divorced , Single).
  - **EmpDepartment** is the department of employee in which they working.
  - **EmpJobRole** shows the position of employee.
  - **BusinessTravelFrequency** means how many times the employee travels for the field or near to clients.
  - **DistanceFromHome** is how far the employee stays from the company.
  - **EmpEducationLevel** is the highest qualification of employee.
  - **EmpEnvironmentSatisfaction** is a rating about the work culture or Environment in which they works.
  - **EmpHourlyRate** shows how much time employee works in a day.
  - **EmpJobInvolvement** is the  employee's emotional investment in their work.
  - **EmpJobLevel** is the employee's position within the organization.
  - **EmpJobSatisfaction** is level of job satisfaction that employees experience in their current roles.
  - **NumCompaniesWorked** shows that how many companies the employee worked before.
  - **OverTime** indicating whether an employee works beyond their regular hours.
  - **EmpLastSalaryHikePercent**  percentage increase in an employee's salary during their most recent salary hike.
  - **EmpRelationshipSatisfaction** shows that the relationships with colleagues, supervisors, and team members.
  - **TotalWorkExperienceInYears** is the number of years of work experience that an employee has accumulated throughout their career.
  - **TrainingTimesLastYear** is the number of times an employee received training in the last year.
  - **EmpWorkLifeBalance** shows that how well an employee can manage their professional and personal commitments.
  - **ExperienceYearsAtThisCompany** indicates the number of years an employee has worked at their current company.
  - **ExperienceYearsInCurrentRole** represent the number of years an employee has spent in their current job role or position within the organization.
  - **YearsSinceLastPromotion** indicates the number of years that have elapsed since an employee's last promotion within the organization.
  - **YearsWithCurrManager** shows that the number of years an employee has worked under their current manager.
  - **Attrition** used to determine whether an employee has left the organization or is still employed.
### ii) **Project Workflow**
#### 1. **Exploratory Data Analysis (EDA)**
- Data loading
- Data visualization using Matplotlib & Seaborn
#### 2. **Data Pre-processing**
- Checking null values
- Checking duplicates
- Checking corrupted values
- Identifying & Handling the outliers (Boxplot & Winsorize)
- Handling skewness (Log1p Transformation)
- Encoding categorical features (LabelEncoder)
- Feature scaling (MinMaxScaler)
- Feature selection
- Feature Balancing (SMOTE)
- Splitting dataset into training & testing sets (train_test_split)
  
#### 3. **Machine Learning Models**
The project implements multiple machine learning models & one deep learning model for multi-class classification:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- K-Neighbors Classifier(KNN)
- Support Vector Classifier(SVC)
- Multi-layer Perceptron (MLP) Classifier

#### 4. **Hyperparameter Tuning**
- GridSearchCV is used to optimize model parameters.

#### 5. **Model Evaluation**
- Accuracy Score
- Confusion Matrix
- Classification Report

#### 6. **Results**
The performance of the models are as follows:  

| **Model**                  | **Accuracy**  |
|----------------------------|---------------|
| **Random Forest Classifier** | **95%**    |
| **GradientBoostingClassifier** | **93.75%**   |
| **DecisionTreeClassifier** | **89.58%**   |
| **MLPClassifier** | **88.33%**   |
| **SVC** | **84.58%**   |
| **LogisticRegression** | **77.5%**   |
| **KNeighborsClassifier** | **65.42%**   |

---
# **Goals and Insights**
## 1. **Department-wise Performance**
- **Top Performing Departments**:
  - Development (3.08)
  - Data Science (3.05)
- **Lowest Performing Departments**:
  - Sales (2.86)
  - Finance (2.77)

## 2. **Top 3 Factors Effecting Employee Performance**
- **EmpEnvironmentSatisfaction** (0.40 correlation) - Employees who rate their work environment highly tend to perform better.
- **EmpLastSalaryHikePercent** (0.33 correlation) - Higher salary hikes are linked to better performance.
- **YearsSinceLastPromotion** (0.25 correlation) - Employees who go longer without a promotion tend to perform worse.

## 3. **Employee Performance Prediction Model**
- **Best Model**: **Random Forest Classifier**
- **Accuracy Achieved**: 95%
- **Usage**: Predicts employee performance based on input factors, aiding in hiring and training decisions.

## 4. **Recommendations**
- **Improve Workplace Environment** - Enhance employee engagement and work-life balance initiatives.
- **Performance-Based Salary Hikes** - Implement a transparent system linking salary hikes to performance.
- **Frequent Promotions & Career Growth Plans** - Encourage employee motivation through structured career progression.
- **Targeted Training for Low-Performing Departments** - Finance and Sales teams should undergo specialized training.
- **Data-Driven Hiring** - Use the predictive model to hire high-potential employees.

---
## **Conclusion**
By implementing these recommendations, INX Future Inc. can further enhance employee performance, engagement, and satisfaction, leading to a more productive and successful organization
