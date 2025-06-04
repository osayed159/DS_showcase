# Churn Prediction Analysis

This project implements a churn prediction system using both traditional machine learning models and GPT-2 language model. The analysis is performed on user activity data from a game platform.

## Features

- Data preprocessing and feature engineering
- Multiple ML models (Decision Tree, Random Forest, Logistic Regression)
- GPT-2 based predictions
- Comprehensive model evaluation
- Feature importance analysis

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

4. Download and prepare the data:
   - Download the datasets from [Churn Prediction Datasets](https://tinyurl.com/pchurndatasets):
     - `playerLogs_game2_playerbasedlines.jsonl.zip` (247.2 MB)
     - `rawdata_game1.csv` (4.6 MB)
     - `playerLogs_Documentation_ChurnPredictionPaper.pdf` (7.1 MB)
   - Extract the files to the `data/game2_processed/` directory
   - The notebook will automatically process and split the data

## Project Structure

```
churn_predictor/
├── README.md           # Project documentation
├── requirements.txt    # Project dependencies
├── src/               # Source code
│   └── __init__.py
├── data/              # Data files (not included in repo)
│   └── game2_processed/  # Processed data files
└── notebooks/         # Jupyter notebooks
    └── Assignment13.ipynb  # Main analysis notebook
```

## Data Requirements

The project uses two datasets for churn prediction analysis:

### Game2 Dataset
The main dataset contains user activity data from a mobile game. The dataset includes:
- User activity timestamps
- Play counts and session information
- Scores and rewards
- In-game events and actions

#### Dataset Files
1. Input file: `data/game2_processed/playerLogs_game2_playerbasedlines.jsonl`
   - Download: [Game2 Player Logs](https://tinyurl.com/pchurndatasets)
   - Format: JSONL (JSON Lines)
   - Size: 247.2 MB (compressed)
   - Documentation: [Churn Prediction Paper](https://tinyurl.com/pchurndatasets)

2. Generated files (created by the notebook):
   - `data/game2_processed/train.jsonl` (80% of data)
   - `data/game2_processed/test.jsonl` (20% of data)
   - `data/game2_processed/train_features.csv` (processed features)
   - `data/game2_processed/test_features.csv` (processed features)

### Game1 Dataset
Additional dataset for comparative analysis:
- File: `rawdata_game1.csv`
- Size: 4.6 MB
- Format: CSV
- Contains similar user activity data for a different game


## Models

The project implements several models for churn prediction:

1. Traditional ML Models:
   - Decision Tree
   - Random Forest
   - Logistic Regression

2. GPT-2 Language Model:
   - Converts user data to natural language prompts
   - Generates churn predictions

## Results

The analysis shows that:
- Traditional ML models perform better than GPT-2 for this task
- Most important features are:
  - Days since last play
  - Active days
  - Play count
- GPT-2 shows potential but needs more tuning

## Future Improvements

Potential areas for improvement:
1. Feature engineering: Add more temporal features
2. Model tuning: Optimize hyperparameters
3. GPT-2: Improve prompt engineering
4. Ensemble methods: Combine predictions from different models 