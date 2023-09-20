# CODSOFT_TITANIC_SURVIVAL-PREDICTION
#importing libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix

%matplotlib inline

# loading dataset
df = pd.read_csv('sag.csv')
df

train = pd.read_csv('sag.csv')
test = pd.read_csv('sag.csv')
#num of rows and coloumns
train.shape

#loading of info()
train.info(10)

#checking null values in dataset sag.csv
train.isnull().sum()

#Gender Plot
unique_genders = df['Gender'].unique()
print(unique_genders)


#index Check the actual column names in the dataset
print(train.columns)






#pie chart represting Count of survivors & Non_ Survivors
survived_counts = train['Survived'].value_counts()
plt.figure(figsize=(6, 6))
plt.pie(survived_counts, labels=['Did Not Survive', 'Survived'], autopct='%1.1f%%', startangle=90, colors=['lightcoral', 'lightgreen'])
plt.title('Survivors vs. Non-Survivors')
plt.axis('equal')
plt.show()
