# Overview
MLAnalyzer is a software able to read a CSV file given by the user and perform analysis on different supervisioned AI classification models and optimization techniques, comparing the resulting F1-Score, processing time, area under the ROC curve, memory usage, precision, accuracy and recall.

The results of the analysis are provided in the program though a series of graphs and be extracted at the results table folder (CSV and XLSX formats) and results image folder (PNG and PDF formats). 

You can test your own AI model, check the "custom AI model" folder. In adittion, you can configurate the optimization of the Grid-Search and Random-Search, check the read_me at the "configurate optimization" folder.

List of models:
- Naive Bayes
- SVM
- MLP
- Decision Tree
- KNN
- Logaritimic Regression
- GradientBoost
- XGBoost
- Custom AI Model

List of dimension reduction techniques:
- PCA
- Incremental PCA
- ICA
- LDA

Run the .exe file to execute the software, it wraps a .jar file that runs the java script.

You can modify it at will and run the modified version by running the java script manually. In case you are using VSCode, remember to open the entire folder instead of only the java file

Click on this video for an exemple of the usage of the program. Skip to 11:45 for the results
[![Watch the video](https://img.youtube.com/vi/J5QUgqYNB_4/maxresdefault.jpg)](https://youtu.be/J5QUgqYNB_4)


# Installation 
Prior to running the program, ensure the following dependencies are installed on your device:
- Java Development Kit (JDK) and Java Runtime Environment (JRE)
- Python 3

Additionally, install the necessary Python libraries by executing the following command in your terminal:
```
pip install matplotlib seaborn pandas numpy scikit-learn pillow psutil xgboost reportlab openpyxl scipy
```

# Default Data Cleaning
Some data changes are very basic or essential for the all the models to work and are done by default, those being:
- Removing the id column if present
- Data suffling
- Turning numerical strings into int or float
- Dropping lines with NaN
- use of OneHotEncoder in columns that have less than 10 unique values
- Applying LabelEncoder()

# ATENTION
- Your CSV must allow for supervisioned classification AIs.
- The target variable (y) column must be the last column of the CSV.
- In case the program generates an error, the details will be stored at the file error_log.txt
