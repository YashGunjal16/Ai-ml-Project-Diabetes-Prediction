# Diabetes Prediction using Machine Learning

![Test Image 1](https://res.cloudinary.com/grohealth/image/upload/c_fill,f_auto,fl_lossy,h_650,q_auto,w_1085/v1581695681/DCUK/Content/causes-of-diabetes.png)

Diabetes, is a group of metabolic disorders in which there are high blood sugar levels over a prolonged period. Symptoms of high blood sugar include frequent urination, increased thirst, and increased hunger. If left untreated, diabetes can cause many complications. Acute complications can include diabetic ketoacidosis, hyperosmolar hyperglycemic state, or death. Serious long-term complications include cardiovascular disease, stroke, chronic kidney disease, foot ulcers, and damage to the eyes.

This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of the dataset is to diagnostically predict whether or not a patient has diabetes, based on certain diagnostic measurements included in the dataset. Several constraints were placed on the selection of these instances from a larger database. In particular, all patients here are females at least 21 years old of Pima Indian heritage.

# Objective
We will try to build a machine learning model to accurately predict whether or not the patients in the dataset have diabetes or not?

# Details about the dataset
The datasets consists of several medical predictor variables and one target variable, Outcome. Predictor variables includes the number of pregnancies the patient has had, their BMI, insulin level, age, and so on.

# Result 
The model created as a result of XGBoost hyperparameter optimization became the model with the lowest Cross Validation Score value. (0.90)


3. LightGBM
LightGBM (Light Gradient Boosting Machine) is a gradient boosting framework designed for speed and efficiency, especially with large datasets.

Key Features:
Handles large datasets and high-dimensional data efficiently.
Uses a novel technique called leaf-wise growth for faster training and better accuracy.
Supports both classification and regression tasks.
Advantages:
Faster training compared to other gradient boosting models (like XGBoost).
Lower memory usage.
Handles missing values automatically.

StandardScaler(): Scales the features to have a mean of 0 and a standard deviation of 1. This is important because SVM is sensitive to the scale of the input features.
scaler.fit_transform(X_train) computes the mean and standard deviation of the training data (X_train) and scales it accordingly.
scaler.transform(X_test) applies the same scaling to the test data (X_test), ensuring consistency.

Total Sum of Squares (ss_total): This represents the total variation in the dependent variable y (Glucose) around its mean. It's calculated as:
𝑠
𝑠
𝑡
𝑜
𝑡
𝑎
𝑙
=
∑
(
𝑦
𝑖
−
𝑦
ˉ
)
2
ss 
total
​
 =∑(y 
i
​
 − 
y
ˉ
​
 ) 
2
 
Where 
𝑦
𝑖
y 
i
​
  is each observed value of y, and 
𝑦
ˉ
y
ˉ
​
  is the mean of y.

Residual Sum of Squares (ss_residual): This represents the variation in the dependent variable y that is not explained by the regression model. It's calculated as:
𝑠
𝑠
𝑟
𝑒
𝑠
𝑖
𝑑
𝑢
𝑎
𝑙
=
∑
(
𝑦
𝑖
−
𝑦
^
𝑖
)
2
ss 
residual
​
 =∑(y 
i
​
 − 
y
^
​
  
i
​
 ) 
2
 
Where 
𝑦
𝑖
y 
i
​
  is each observed value of y, and 
𝑦
^
𝑖
y
^
​
  
i
​
  is each predicted value of y based on the model.

R² Score: The R² score measures the proportion of the variance in y that is explained by the regression model. It is calculated as:
𝑅
2
=
1
−
𝑠
𝑠
𝑟
𝑒
𝑠
𝑖
𝑑
𝑢
𝑎
𝑙
𝑠
𝑠
𝑡
𝑜
𝑡
𝑎
𝑙
R 
2
 =1− 
ss 
total
​
 
ss 
residual
​
 
​
 
If 
𝑅
2
R 
2
  is close to 1, it indicates that the model explains most of the variance in the data.
If 
𝑅
2
R 
2
  is close to 0, it indicates that the model does not explain much of the variance.
