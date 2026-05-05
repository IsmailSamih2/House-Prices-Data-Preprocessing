# House Prices: Advanced Regression - Data Preprocessing

### Project Overview
This project completes the first assignment for the Machine Learning course. It focuses on the comprehensive data preprocessing of the "House Prices: Advanced Regression Techniques" dataset from Kaggle. The goal is to prepare a clean and engineered training set ready for regression modeling.

### Dataset
- **Source:** Kaggle House Prices Competition.
- **Context:** 79 explanatory variables describing residential homes in Ames, Iowa.
- **Target:** `SalePrice`.

### Implemented Tasks

#### 1. Data Retrieval
- Loaded `train.csv` and `test.csv` using `pandas`.
- Conducted dataset inspection (dimensions and head).
- Implemented memory management by optimizing column data types (downcasting and categorical conversion).

#### 2. Data Cleaning
- **Missing Values:** Analyzed significant missing data (PoolQC, MiscFeature, Alley, etc.) and applied appropriate filling strategies (e.g., treating NaN as "No Pool/None").
- **Outlier Removal:** Identified extreme observations in `GrLivArea` vs `SalePrice` and removed them to improve model stability.
- **Data Transformation:** Applied logarithmic transformation (`np.log1p`) to the target variable `SalePrice` to normalize its right-skewed distribution.

#### 3. Exploratory Data Analysis (EDA)
- **Correlation:** Created a correlation matrix and heatmap to identify the top 5 features most correlated with price.
- **Visualizations:**
  - Scatter plots of `GrLivArea` vs `SalePrice` colored by `OverallQual`.
  - Visualized average prices across different neighborhoods to gain geographical insights.

#### 4. Feature Engineering
- **Feature Creation:** Engineered a new feature `TotalSF` (Total Square Footage) by combining basement and floor areas.
- **Encoding:**
  - Applied **Label Encoding** for ordinal features (e.g., Quality and Condition) to preserve rankings.
  - Applied **One-Hot Encoding** for nominal features (e.g., Neighborhood, BldgType).
- **Pipeline:** Encapsulated the preprocessing logic into a reusable function to ensure consistency across training and testing sets.

### How to Run
1. Ensure the dataset files are placed in a `/data` folder.
2. Install dependencies listed in `requirements.txt`.
3. Run the Jupyter Notebook from start to finish (One-Click Run).
