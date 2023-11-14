# Student Performace Prediction - MLOPs Project

Welcome to the Student Performance Analysis and Test Score Prediction project! Education is a multifaceted journey influenced by various factors, and understanding these dynamics is crucial for fostering an inclusive and effective learning environment. This project aims to unravel the intricate relationship between student performance and key variables such as Gender, Ethnicity, Parental Level of Education, Lunch Type, and Test Preparation Course.

## 📦 Dataset information 

The dataset for this project is sourced from Kaggle and is available at [Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?datasetId=74977). It comprises 1000 rows and 8 columns, each providing valuable insights into student performance.

### Columns in the Dataset:

1. **gender**: Sex of students (Male/Female)
2. **race/ethnicity**: Ethnicity of students (Group A, B, C, D, E)
3. **parental level of education**: Parents' final education (Bachelor's Degree, Some College, Master's Degree, Associate's Degree, High School)
4. **lunch**: Whether the student had lunch before the test (Standard or Free/Reduced)
5. **test preparation course**: Completion status of the test preparation course (Complete or Not Complete)
6. **math score**: The score obtained in the math test
7. **reading score**: The score obtained in the reading test
8. **writing score**: The score obtained in the writing test


## 🐍 Python Requirements & Set up

Let's jump into the Python packages you need. Within the Python environment of your choice, run:

```python
git clone https://github.com/Basavachari/studentPerformance.git
cd studentPerformance
pip install -r requirements.txt
```
To run the front end of the application, run the following command in the terminal:
```python
python app.py
```

## CI/CD Pipeline with Azure Pipelines
1. Login to Azure DevOps.
2. Create a resouse of Web App.
3. Add the name for webapp and select runtime for Python 3.8
4. Enable the github actions and configure with your github account and choose the repository.
5. Review and create.
6. Open the github actions in your repository, where you can see the deployment link.

## 🚀 Training Pipeline
The training pipeline for this project is
- `ingest`: Ingests the data from csv file in artifacts folder.
- `transformation`: Transforms the data by scaling, categorical encoding and saves the compelete preprocess step in artifacts folder.
- `split`: Splits the dataset into train and test splits.
- `train`: Trains the model on the training split and saves the model in artifacts folder.
- `evaluate`: Evaluates the model on the eval split.

- `predict`: Predicts the data given by the user using the model saved in artifacts folder.
- `deploy`: Deploys the model using flask and creates a web app.

## Demo 
<!-- add the link of deplyment -->
[![Deployed App](https://img.shields.io/badge/Deployed%20App-Student%20Performance%20Prediction-blue)](https://studentprediction.azurewebsites.net/)