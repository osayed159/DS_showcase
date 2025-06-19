# Car Price Analysis Project

## Overview
This project analyzes factors affecting car prices using a dataset from Kaggle. The analysis includes exploratory data analysis (EDA) and machine learning models to predict car prices based on various features.

## Dataset
- **Source:** [Kaggle Car Price Prediction Dataset](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction)
- **Size:** 250 entries with 26 features
- **Features Include:**
  - Car specifications (engine size, horsepower, etc.)
  - Physical attributes (length, width, height)
  - Categorical features (fuel type, body type, etc.)
  - Target variable: Price

## Project Structure
```
Car_Prices/
├── data/                  # Dataset files
├── notebooks/            # Jupyter notebooks
│   └── eda_car_price.ipynb
├── images/              
├── requirements.txt     # Project dependencies
└── README.md           # Project documentation
```

## Setup and Installation
1. Clone the repository

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Analysis Components
1. **Exploratory Data Analysis (EDA)**
   - Data quality checks
   - Feature distribution analysis
   - Correlation analysis
   - Visualization of key relationships

2. **Feature Analysis**
   - Categorical variables (fuel type, body type, etc.)
   - Numerical variables (engine size, horsepower, etc.)
   - Price distribution and relationships

3. **Model Training and Evaluation**
   - Data preprocessing: scaling and encoding features
   - Splitting data into training and test sets
   - Training a linear regression model to predict car prices
   - Evaluating model performance (R-squared and other metrics)
   - Interpreting results and feature importance

## Key Findings
- **Brand and Market Segment:** Luxury brands (e.g., Porsche, Jaguar, BMW) have the highest median prices, while economy brands (e.g., Mazda, Mitsubishi, Dodge) show lower median prices. Brand is a significant factor in car pricing, with clear separation between luxury and economy segments.
- **Physical and Performance Features:** Car width, length, wheelbase, engine size, horsepower, and curb weight all show strong positive correlations with price. Larger and more powerful vehicles command premium pricing.
- **Fuel Efficiency:** Higher city and highway MPG are negatively correlated with price, indicating that more fuel-efficient cars tend to be less expensive.
- **Body and Engine Type:** Hardtop and OHV engine types are associated with higher prices, while hatchbacks and OHC/OHCF engines are generally more affordable. Sedans and OHC engines show the most price diversity.
- **Model Performance:** The linear regression model achieved an R-squared score of approximately 0.84 on the test set, indicating good predictive power for car prices based on the selected features.

## Tools and Technologies
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Plotly

## Contributing
Feel free to submit issues and enhancement requests.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
