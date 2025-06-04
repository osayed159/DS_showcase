# Churn Predictor

This repository contains the code and resources for the Churn Predictor project.

## Setup Instructions

1. Create a virtual environment:
   ```bash
   python -m venv venv
   ```

2. Activate the virtual environment:
   - Windows:
     ```bash
     .\venv\Scripts\activate
     ```
   - Unix/MacOS:
     ```bash
     source venv/bin/activate
     ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Project Structure

```
Churn_predictor/
├── README.md           # This file
├── requirements.txt    # Project dependencies
├── src/               # Source code
│   └── __init__.py
└── notebooks/         # Jupyter notebooks
```

## Getting Started

1. After setting up the environment, you can start Jupyter notebook:
   ```bash
   jupyter notebook
   ```

2. Navigate to the `notebooks` directory to create or open notebooks for your analysis.

## Notebook Overview

The notebook `Assignment12.ipynb` performs the following tasks:

1. **Data Splitting**: It splits JSON files into training and testing datasets.
2. **Feature Extraction**: It extracts features from user event data for churn prediction, including:
   - Play count
   - Active days
   - Mean score
   - Score standard deviation
   - Best score
   - Days since last play
   - Average session gap
   - Last 7 days activity
   - Churn label
3. **Data Preparation**: It prepares the model dataset by processing JSONL files and writing extracted features to CSV.
4. **Model Training**: The notebook trains multiple classifiers, including:
   - Decision Tree
   - Random Forest
   - Logistic Regression
5. **Model Evaluation**: It evaluates the models using classification metrics and feature importance analysis.
6. **LLM Churn Prediction**: The notebook generates prompts for a Language Model (LLM) to predict churn based on user data. It processes user information and classifies whether a user will churn or not.
7. **Data Saving**: The notebook saves the processed datasets in JSONL format for further use.

This notebook is essential for preparing the data, training the churn prediction model, and generating predictions using an LLM.

## Datasets

The following datasets are required for the Churn Predictor project:

- **Game 1 Dataset**: [Download Game 1 Dataset](https://tinyurl.com/pchurndatasets)
- **Game 2 Dataset**: [Download Game 2 Dataset](https://tinyurl.com/pchurndatasets)

Please ensure to download and place these datasets in the `data/` directory as specified in the project structure. 