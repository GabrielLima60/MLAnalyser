# Overview
Best-Classification-AI is a software able to read a CSV file given by the user and perform analysis on different supervisioned AI classification models and optimization techniques, comparing the resulting F1-Score, processing time, area under the ROC curve, memory usage, precision, accuracy and recall.

The results of the analysis are provided in the program though a series of graphs and be extracted at the results table and results image folders. 

You can configurate the optimization of the Grid-Search and Random-Search, check the read_me at the "configurate optimization" folder.

You can test your own AI model, check the "custom AI model" folder.

Run the .exe file to execute the software. 
You can modify it at will and run the modified version though the java script.

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
