# SMedia-_usage
Abstraction
•	Using a dataset that includes App type, Likes per Day, Minutes Spent, Posts per Day, and Follows per Day, this study examines social media activity across several platforms. Evaluating user engagement, retention, and activity patterns was the goal.
•	This was accomplished by classifying overall social media activity using the Random Forest Classifier. Create an Engagement class feature with Low, High, and Medium categories for this purpose.
•	Posts per day and follows per day were modeled using regression techniques, while Likes per day were predicted using the XGBoost Regressor.
•	The identification of active users (high posting and following behavior) was used to gauge user activity.
•	The relationship between follower increases and time spent was investigated through retention analysis.
•	Likes received in relation to posting frequency were used to gauge engagement levels.
# Import Libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_absolute_error
from sklearn.metrics import mean_absolute_percentage_error
from xgboost import XGBRegressor
from sklearn.metrics import mean_squared_error
from sklearn.metrics import root_mean_squared_error
from sklearn.linear_model import LinearRegression
from sklearn.metrics import r2_score
# Import CSV file
Import CSV file which took from Kaggle. 
<img width="1513" height="581" alt="image" src="https://github.com/user-attachments/assets/78958454-762b-46d4-ba5d-c49068295bd4" />
# Preprocessing (by using wrangler)
<img width="1523" height="606" alt="image" src="https://github.com/user-attachments/assets/2bb04a20-3a67-45b7-bbb2-9600ff432331" />
perform some processing on data for making object column (app) to int.
# Define high vs low engagement
Create an Engagement class feature with Low, High, and Medium categories.
# Features & Target
Do feature engeenering so that separate dependent and independent variables.
# Split the data
Split the data ,80% for training and 20% for testing.
# Predictive Model
Apply Random Forest Classifier model.
# Evaluation
<img width="1087" height="504" alt="image" src="https://github.com/user-attachments/assets/82604a27-1531-40ad-b695-1a45bde814cd" />
# Conclusion
Accuracy = 70%
Predicted Low Engagement with social media= 32%
Actual Low Engagement with social media = 12%
High Engagement of social media(predicted) = 76%
High Engagement of social media(actual) = 91%
This result shows many people engage with social media.
# Visualisation of top active Apps on the base of Posts and Follows
<img width="895" height="547" alt="image" src="https://github.com/user-attachments/assets/10c23a77-0659-4444-9a62-6dfd027bb34a" />
# To find Active user on the base of Post per day ,likes per day,follows per day
For this purpose i applied XGBregressor model.
# Feature,target and split the data for Post per day ,likes per day,follows per day
 # Evaluation of post per day
 i use MAE metrics to evaluate the error between actual and predicted data
 <img width="526" height="65" alt="image" src="https://github.com/user-attachments/assets/3b746099-8455-4925-b0fe-1b8721c11d4e" />
 The error is 5 while maximum post per day is 20 so it is normal error not higher.
 # Visualisation of Average posts per day by App
 <img width="686" height="470" alt="image" src="https://github.com/user-attachments/assets/d7be1124-7e84-4066-8bbc-ef524a6c9238" />

  # Evaluation of follows per day
  <img width="526" height="56" alt="image" src="https://github.com/user-attachments/assets/32c7a0b9-f6cf-4864-8fdc-d3be75786ef7" />
  The error between predicted and actual valwes is 13 whilemaximum follows per day is 50. There is a little bit high error in prediction.
  # Visualisation of follows per day by App
  <img width="686" height="470" alt="image" src="https://github.com/user-attachments/assets/066444c9-ba7d-442b-bb56-56a72a53e0fe" />
   # Evaluation of follows per day
   <img width="543" height="54" alt="image" src="https://github.com/user-attachments/assets/5dfbbd96-acb5-4f3b-8d96-b3de36189ae7" />
   Maximum likes perday is 500 while MAE is 141 which is error between actual and predicted value. it is also high error.
   # Visualisation of follows per day by App
   <img width="686" height="470" alt="image" src="https://github.com/user-attachments/assets/8dbf9276-530e-43f4-9e5b-f399656df61e" />
   # Insights
   <img width="645" height="565" alt="image" src="https://github.com/user-attachments/assets/358f9fd9-7fe5-4b51-8820-bed8d03a826a" />
   According to this visual we can say that the correlation between all features is very weak thats why predicted models are showing error rate high specially likes per day. Users are showing their interest on different platforms regarding their interest .usre mostly like to follow and post the instagram app while he likes the post on facebook platform.  




  
  


 








