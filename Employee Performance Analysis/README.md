## Data Science Project on Employee Performance Analysis

### Business Case:
We must analyze the feautres present in the dataset, establish a correlation between the feautres and employee performance, and forecast the employee performance rating based on the feautres.

### The Goal and Insights of the project are as follows:

#### Department wise performances

Top 3 Important Factors effecting employee performance
A trained model which can predict the employee performance based on factors as inputs. This will be used to hire employees
Recommendations to improve the employee performance based on insights from analysis
With 1200 rows, the provided Employee dataset is large. There are 28 columns of features in the data. The dataset is 1200x28 in size. 19 of the 28 traits, which are divided into qualitative and quantitative categories, are quantitative (11 columns consists numeric data & 8 columns consists ordinal data) and there are 8 qualitative qualities. EmpNumber consists of alphanumeric data (distinct values), which is not a feature that is important for performance evaluation.

Correlation between characteristics and Performance Rating is one of the key aspects of the data that can be obtained via correlation. A statistical measure known as correlation expresses how linearly related two variables are to one another. The project's analysis went through stages of univariate, bivariate, and multivariate analysis, correlation analysis, and analysis by each department to meet the project's objective.

Categorical and numerical data make up the dataset. Since the target variable only contains ordinal values, the issue is one of classification. The Support Vector Classifier, Random Forest Classifier, and Artificial Neural Network [Multilayer Percepton] are the different machine learning models employed in this project. Artificial neural network [Multilayer percepton] predicts with a greater accuracy of 95.80% from the models mentioned above.

Finding the significant factor influencing the performance rating is one of the project's key objectives. The machine learning model feature importance technique was used to forecast the significant characteristics. Because most machine learning techniques rely on numerical approaches, which do not support strings, the major methodology utilized in preprocessing data uses the Mannual & Frequency encoding method to turn string-categorical data into numerical data. The machine learning model and visualization approaches were used to carry out the project as a whole and meet its objectives.

### 1. Requirement
For this initiative, the IABAC served as the source of the data that was provided. Based on information from INX Future Inc. (referred as INX ). With more than 15 years of experience operating internationally, it is one of the top providers of automation and data analytics solutions. Over the last five years, INX has continuously ranked among the top 20 best employers. The information is not from the actual company. The entire project was completed using the Python platform and a Jupyter notebook.

### 2. Analysis
By summarizing the features found in the data, analysis of the data was conducted. In the analysis, the traits are more important. The characteristics reveal how the dependent and independent variables are related. Early on in our study, Pandas also helped to define the datasets and provide answers to the questions below. The dataset's data are broken down into categories and numerical data.

#### Categorical Features
EmpNumber
Gender
EducationBackground
MaritalStatus
EmpDepartment
EmpJobRole
BusinessTravelFrequency
OverTime
Attrition

#### Numerical Features
Age
DistanceFromHome
EmpHourlyRate
NumCompaniesWorked
EmpLastSalaryHikePercent
TotalWorkExperienceInYears
TrainingTimesLastYear
ExperienceYearsAtThisCompany
ExperienceYearsInCurrentRole
YearsSinceLastPromotion
YearsWithCurrManager

#### Ordinal Features
EmpEducationLevel
EmpEnvironmentSatisfaction
EmpJobInvolvement
EmpJobLevel
EmpJobSatisfaction
EmpRelationshipSatisfaction
EmpWorkLifeBalance
PerformanceRating

### 3.Univariate, Bivariate & Multivariate Analysis
Library Used: Matplotlib & Seaborn
Plots Used: Histplot, Lineplot, CountPlot, Barplot
Tip: All Observation or insights written below the plots
Univariate Analysis: In univariate analysis we get the unique labels of categorical features, as well as get the range & density of numbers.

Bivariate Analysis: In bivariate analysis we check the feature relationship with target veriable.

Multivariate Analysis: In multivariate Analysis check the relationship between two veriable with respect to the target veriable.

### CONCLUSION
There are some features are positively correlated with performance rating( Target variable) [Emp Environment Satisfaction,Emp Last Salary Hike Percent,Emp Work Life Balance]

### 4.Exploratory Data Analysis
Basic Check & Statistical Measures
Their is no constant column is present in Numerical as well as categoriacl data.
Distribution of Continuous Features:
Having a general understanding of how the features are distributed among one another would typically be one of the first few steps in exploring the data. We will use the well-known distplot function from the Seaborn plotting package to do this. Both numerical aspects have produced the distribution. It will convey an overall picture of the volume and preponderance of data present at various levels.

The majority of the employees are between the ages of 30 and 40 in the age range of 18 to 60.
Employees have worked for up to eight different companies, with the majority of them having worked for just two before coming to work for us.
The bulk of the workers in this company earn an hourly wage between 65 and 95.
In general, most employees stay with this company for up to five years. In this company, the majority of employees receive wage increases of 11% to 15%.
Check Skewness and Kurtosis of Numerical Features
Checking weather the data is Normally distributed or Not with Skewness and Kurtosis,

YearsSinceLastPromotion, This column is skewed
skewness for YearsSinceLastPromotion: 1.9724620367914252
kurtosis for YearsSinceLastPromotion: 3.5193552691799805
Distribution of Mean of Data
Distribution of mean close to guassian distribution with mean value 9.5
we can say that around 80% feature mean lies between 8.5 to 10.5
Distribution of Standard Deviation of Data
Distribution of standard deviation of data also look like guassian distribution around 30% of feature standard deviation around the range of 3 3 to 20 and remaining 70% feature standard deviation in between 0 to 2

### 5.Data Pre-Processing
1.Check Missing Value: Their is no missing value in data

2.Categorical Data Conversion: Handel categorical data with the help of frequency and mannual encoding, because feature is contain lot's of labels

Mannual Encoding: Mannual encoding is a best techinque to handel categorical feature with the help of map function, map the labels based on frequency.

Frequency Encoding: Frequency encoding is an encoding technique to transform an original categorical variable to a numerical variable by considering the frequency distribution of the data getting value counts.

3.Outlier Handling Some features are contain outliers so we are impute this outlier with the help of IQR because in all features data is not normally distributed

4.Feature Transformation: In YearsSinceLastPromotion some skewed & kurtosis is present, so we are use Square Root Transformation techinque

Square root transformation: Square root transformation is one of the many types of standard transformations.This transformation is used for count data (data that follow a Poisson distribution) or small whole numbers. Each data point is replaced by its square root. Negative data is converted to positive by adding a constant, and then transformed.
Q-Q Plot: Q–Q plot is a probability plot, a graphical method for comparing two probability distributions by plotting their quantiles against each other.
5.Scaling The Data: scaling the data with the help of Standard scalar

Standard Scaling: Standardization is the process of scaling the feature, it assumes the feature follow normal distribution and scale the feature between mean and standard deviation, here mean is 0 and standard deviation is always 1.

### 6.Feature Selection
1.Drop unique and constant feature: Dropping employee number because this is a constant column as well as drop Years Since Last Promotion because we create a new feaure using square root transformation

2.Checking Correlation: Checking correlation with the help of heat map, and get the their is no highly correlated feature is present.

Heatmap: A heatmap is a graphical representation of data that uses a system of color-coding to represent different values.
3.Check Duplicates: In this data Their is no dupicates is present.

4.PCA: Use pca to reduce the dimension of data, Data is contain total 27 feature after dropping unique and constant column,from PCA it shows the 25 feature has less varaince loss, so we are going to select 25 feature.

Principal component analysis (PCA) is a popular technique for analyzing large datasets containing a high number of dimensions/features per observation, increasing the interpretability of data while preserving the maximum amount of information, and enabling the visualization of multidimensional data. Formally, PCA is a statistical technique for reducing the dimensionality of a dataset.
5.Saving Pre-Process Data: save the all preprocess data in new file and add target feature to it.

### 7.Machine learning Model Creation & Evaluation
1.Define Dependant and Independant Features:

2.Balancing the data: The data is imbalance, so we need to balance the data with the help of SMOTE

SMOTE: SMOTE (synthetic minority oversampling technique) is one of the most commonly used oversampling methods to solve the imbalance problem. It aims to balance class distribution by randomly increasing minority class examples by replicating them. SMOTE synthesises new minority instances between existing minority instances.
3.Splitting Training And Testing Data: 80% data use for training & 20% data used for testing

Algorithm:
AIM: Create a sweet spot model (Low bias, Low variance)

HERE WE WILL BE EXPERIMENTING WITH THREE ALGORITHM

Support Vector Machine
Random Forest
Artificial Neural Network [MLP Classifier]
Support vector machine well perform on training data with accuracy 96.61% but the test score is 94.66 after applying Hyperparameter tunning score is 98.28 means model is overfit.
Random forest very well perform in training data with 100% accuracy but in testing 95.61% after doing hyperparameter tunning testing score is decreases.
Artifical neural network[Multilayer percepton] perform very well on training data with 98.95% accuracy and testing score is 95.80%.
So we are select Artifical neuranl network [Multilayer percepton] model.


### Goal 1: Department Wise Performances
PLOT USED

Violinplot: It shows the distribution of quantitative data across several levels of one (or more) categorical variables such that those distributions can be compared.
CountPlot: countplot is used to Show the counts of observations in each categorical bin using bars.
Sales: The Performace rating level 3 is more in the sales department. The male performance rating the little bit higher compared to female.

Human Resources: The majority of the employees lying under the level 3 performance . The older people are performing low in this department. The female employees in HR department doing really well in their performance.

Development: The maximum number of employees are level 3 performers. Employees of all age are performing at the level of 3 only. The gender-based performance is nearly same for both.

Data Science: The highest average of level 3 performance is in data science department. Data science is the only department where less number of level 2 performers. The overall performance is higher compared to all departments. Male employees are doing good in this department.

Research & Development: The age factor is not deviating from the level of performance here where different employees with different age are there in every level of performance. The R&D has the good female employees in their performance.

Finance: The finance department performance is exponentially decreasing when age increases. The male employees are doing good. The experience factor is inversely relating to the performance level.

### Goal 2: Top 3 Important Factors effecting employee performance
The top three important features affecting the performance rating are ordered with their importance level as follows,

Employment Environment Satisfaction
Employee Salary Hike Percentage
Experience Years In CurrentRole
Employee Enviroment satisfaction: Maximum Number of Employees Performance Rating belongs to EmpEnvironmentSatisfaction Level 3 & Level 4, It contains 367 & 361.

Employee last salary hike percent: More Number of Employees whose salary hike percentage belongs to 11-19 % are getting 2 & 3 performance rating Maximum time. as well asEmployees whose salary hike percentage is in between 20-22%, There performance rating is 4.

Employee work life balance: In EmpWorkLifeBalance, level 3 is showing high Performance Rating of employees

### Goal 3: A Trained model which can predict the employee performance
The trained model is created using the machine learning algorithm as follows with the accuracy score,

Support Vector Classifier: 98.28% accuracy
Random Forest classifier: 95.61% accuracy
Artifical Neural Network [Multilayer percepton]: 95.80%
Goal 4: Recommendations to improve the employee performance
The overall employee performance can be achieved by employee environment satisfaction. The company needs to focus more on the employee environment satisfaction.
The salary hike will give the boost to the employees to perform well.
Promote the employee ervery 6th month
Improve Employee's work-life balance this affects the performance rating.
While recruiting for HR, consider the female candidates where they perform well compared to male.
The development and sales department is having an overall higher performance comparing to rest of the departments. While some of the employees who gives feedback like Low & Medium from Job Satisfaction & Relationship Satisfaction feature, such employees gives Excellent performance more in number. So company should focus on them.
