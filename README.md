## **Machine learning project Salifort-Motors**
---
## **Project Overview**:
This project performs Data cleaning, Exploratory Data Analysis, Visualizations, Feature engineering and build predictive models that can provide insights to the HR Department of the company.Python libraries such as Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn.

---
## **Plan Stage**:
## **Objective**:
1. Empower the HR department with predictive insights to enhance employee satisfaction and reduce attrition rate.
2. Perform data cleaning, exploratory data analysis (EDA), feature engineering to uncover key factors influencing employee turnover.
3. Build and compare multiple machine learning models — Logistic Regression, Decision Tree, and Random Forest — to predict attrition.
4. Evaluate models using industry-standard metrics (Accuracy, Precision, Recall, F1-score, and AUC) for reliable performance assessment.
5. Final stage is to find out the best model to be predicted for future insights.
   
---
## **Dataset**:
This dataset contains 14999 rows and 10 columns:
   - **satisfaction_level**: Employee-reported job satisfaction level [0-1]
   - **last_evaluation**: Score of employee’s last performance review[0-1]
   - **number_project**: Number of projects employee contributes
   - **average_monthly_hours**: Average number of hours employee worked per month
   - **time_spend_company**: How long the employee has been with the company (years)
   - **Work_accident**: Whether or not the employee experienced an accident while at work
   - **left**: Whether or not the employee left the company
   - **promotion_last_5years**: Whether or not the employee was promoted in the last 5 years
   - **Department**: Employee's department
   - **salary**: Employee's salary(USD)
     
---
## **Analyze Stage**:
## **Data cleaning**:
1. Gather basic information about data and descriptive statistics.
2. Check for missing values,there is no missing value and there are 3008 rows are duplicated, this is 20% of data.
3. Check a box plot to visualize distribution of 'tenure' to detect outliers.
   
---
## **EDA**:
1. Begin by understanding how many employees left and what percentage of employees represents.
2. There are 1991 employees left which is 16% of total employees.
3. Create box plot to show **average_monthly_hours** distributions for **number_project**,comparing the distribution of employees who stayed or left.
4. Create scatter plot to show **average_monthly_hours** versus **satisfaction_level**.
5. Examine the salary levels of each tenure for further explorations.
6. How many employees left regarding each department by creating stacked histogram chart.
7. Check for strong correlation between variables in the data by creating Heatmap chart.
   
---
## **Construct Stage**:
## **Model Building**:
### **Logistic Regression model**:
1. Determine which model are more appropiate for this project.
2. The process involves binary classification so we could go with Logistic Regression or Tree-based model.
3. Split the data into Training and Testing,create X(variables) and y(outcome variables) for modeling.
4. Construct the Logistic regression model and fit the data into training set.
5. Create a confusion matrix to visualize the result of logistic regression model.
6. The classification report above shows that the logistic regression model achieved a **precision of 79%, recall of 82%, f1-score of 80% (all weighted averages), and accuracy of 82%**.
### **Tree-based model**:
1. First select the feature variables of (X) and isolate the outcome variable of (y).
2. Split the data into Training,Validation and Testing sets.
### **Decision tree**:
1. Construct the Decision tree model and setup the cross validated grid-search to search for best parameters.
2. Fit the Decision tree model to the training data.
3. Find the optimal values **{'max_depth': 4, 'min_samples_leaf': 5, 'min_samples_split': 2}** and check best **AUC score of 0.969819392792457** which is stronger.
4. All scores from grid search cv  **model:decision tree  precision:0.914552  recall:0.916949  F1:0.915707  accuracy:0.971978  auc:0.969819**
5. Indicates strong performance metrics of decision tree.





