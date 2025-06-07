# Churn Predictor

This repository contains the code and resources for the Churn Predictor project. An assignment that was required as part of a course in my master's program.
It was for developing churn predictions for 2 freemium games.

## Setup Instructions(skip if you don't want to work in a virtual env)

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

## Notebooks Overview

The project contains two notebooks:

### 1. Assignment1.ipynb
This notebook contains the complete analysis for Game 1:

1. **Data Processing**:
   - Loading and splitting player data (80% train, 20% test)
   - Feature extraction including:
     - Play count
     - Active days
     - Total playtime
     - Mean score and standard deviation
     - Best score
     - Days since last play
     - Average session gap
     - Last 7 days activity

2. **Model Development**:
   - Training multiple classifiers:
     - Decision Tree
     - Random Forest
     - Logistic Regression
   - Model evaluation using classification metrics
   - Feature importance analysis

### 2. Assignment12.ipynb
This notebook contains the analysis for Game 2 with both traditional ML and LLM approaches:

1. **Data Processing**:
   - JSONL file splitting (80% train, 20% test)
   - Feature extraction including:
     - Play count
     - Active days
     - Mean score
     - Score standard deviation
     - Best score
     - Days since last play
     - Average session gap
     - Last 7 days activity

2. **Traditional ML Analysis**:
   - Training multiple classifiers
   - Feature importance analysis
   - Model evaluation using classification metrics

3. **LLM-based Analysis**:
   - Integration with GPT-2 model
   - Generation of user-specific prompts
   - LLM-based churn prediction
   - Analysis of LLM predictions with behavioral weights
   - Note: Limited to 500 users for LLM analysis due to computational constraints

Note: Due to computational constraints, the Game 2 analysis is limited to:
- 10,000 lines for training
- 5,000 lines for testing
- 500 users for LLM analysis

## Datasets

The following datasets are required for the Churn Predictor project:

- **Game 1 Dataset**: [Download Game 1 Dataset](https://tinyurl.com/pchurndatasets)
- **Game 2 Dataset**: [Download Game 2 Dataset](https://tinyurl.com/pchurndatasets)

Please ensure to download and place these datasets in the correct directory and adjust paths accordingly in the notebooks.

## Running the Analysis

You need to run both notebooks to get the complete analysis:

1. **Assignment1.ipynb** for Game 1 analysis
2. **Assignment12.ipynb** for Game 2 analysis (includes both traditional ML and LLM approaches)

For both notebooks:
- Run cells in sequence as they build upon each other
- Each notebook contains detailed comments and explanations
- Make sure to adjust file paths according to your setup

## Output Files

The analysis generates several output files:

### Game 1
- `data/game1_processed/ds1_train.csv`: Training dataset
- `data/game1_processed/ds2_test.csv`: Test dataset
- `data/game1_processed/ds2_with_predictions.csv`: Test predictions

### Game 2
- `data/game2_processed/train.jsonl`: Training data split
- `data/game2_processed/test.jsonl`: Test data split
- Generated feature CSV files for both training and test sets
- LLM predictions for a subset of users
