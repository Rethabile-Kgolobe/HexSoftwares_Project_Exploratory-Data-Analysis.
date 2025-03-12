# HexSoftwares_Project_Exploratory-Data-Analysis.

## Project Overview

This repository contains two distinct data analysis projects:

1.  **Iris Dataset EDA:** An exploratory data analysis of the classic Iris dataset, focusing on understanding feature distributions and species differentiation.
2.  **House Price Prediction:** A project involving data preprocessing, feature engineering, and linear regression modeling to predict house prices using the House Price Prediction dataset.

## Project 1: Iris Dataset EDA

### Dataset Information

The Iris dataset is a classic dataset in machine learning and statistics. It contains 150 instances of iris flowers, with measurements of their sepal length, sepal width, petal length, and petal width (all in centimeters). The goal is to understand the underlying structure of the data, identify potential relationships between features, and gain insights into how these features differentiate the three Iris species: Setosa, Versicolor, and Virginica.

The Iris dataset includes the following features:

*   **Id:** A unique identifier for each flower sample.
*   **SepalLengthCm:** Length of the sepal in centimeters.
*   **SepalWidthCm:** Width of the sepal in centimeters.
*   **PetalLengthCm:** Length of the petal in centimeters.
*   **PetalWidthCm:** Width of the petal in centimeters.
*   **Species:** The species of the iris flower (Setosa, Versicolor, or Virginica).

### Steps Performed

1.  **Data Loading:** The Iris dataset was loaded from a CSV file (`iris.csv`) into a Pandas DataFrame.
2.  **Data Inspection:**

    *   The first few rows of the dataset were displayed to get a sense of the data.
    *   Descriptive statistics (mean, median, standard deviation, etc.) were calculated for each numerical feature to understand their distributions.
    *   The data types of each column were checked to ensure they were appropriate.
    *   Checked the number of rows and columns in the dataset.
3.  **Data Cleaning:**

    *   Checked for missing values using `.isnull().sum()`. No missing values were found.
    *   I removed the `Id` column as it is irrelevant to the analysis.
    *   Checked for duplicate entries. Duplicates were dropped to ensure data quality.
4.  **Exploratory Data Analysis (EDA):**

    *   **Univariate Analysis:** Examined the distribution of individual features using histograms and box plots.
    *   **Multivariate Analysis:**
        *   Scatter plots were created to visualize the relationships between pairs of features.
        *   A pair plot was generated to visualize all pairwise relationships in a single grid.
        *   A correlation matrix was calculated and visualized using a heatmap to identify highly correlated features.

### Tools Used

*   Python
*   Pandas
*   NumPy
*   Matplotlib
*   Seaborn

### Key Findings and Insights

*   **Species Differentiation:** The Iris species can be relatively well separated using petal measurements (length and width). Setosa is notably distinct from Versicolor and Virginica.
*   **Feature Correlations:**

    *   Strong positive correlations exist between petal length and petal width. This suggests that as petal length increases, petal width also increases.
    *   Sepal length and sepal width show a weaker correlation compared to petal dimensions.
*   **Data Distributions:**

    *   Petal length and petal width exhibit apparent differences across the three species, making them good candidates for classification.
    *   Sepal width has more overlap between the species, making it a less reliable feature for distinguishing between them.
    *   
*   **Observations on Species:**

    *   *Iris setosa* tends to have smaller petal lengths and widths but larger sepal widths.
    *   *Iris virginica* tends to have larger petal lengths and widths but smaller sepal widths.
    *   *Iris versicolor* falls in between *Iris setosa* and *Iris virginica* in terms of petal and sepal dimensions.

### Visualizations

*   **Pairplot:** Illustrates the relationships between all pairs of features, with different colors representing different species.

*   **Correlation Heatmap:** Displays the correlation coefficients between numerical features. Darker colors indicate stronger correlations (positive or negative).


### Conclusion

The Exploratory Data Analysis of the Iris dataset revealed significant insights into the characteristics of the different Iris species and the relationships between their sepal and petal dimensions. Petal length and petal width are handy for distinguishing between species, while sepal measurements are less discriminatory. The strong correlation between petal length and width suggests that these features are related and could be used together in predictive models. The insights gained from this EDA can inform the selection of appropriate features and models for classification tasks involving the Iris dataset. Further analysis could include building machine learning models to predict Iris species based on these measurements.

## Project 2: House Price Prediction

### Dataset Information

The House Price Prediction dataset contains information about various features of houses and their corresponding sale prices. The goal is to build a model that can accurately predict the sale price of a house based on its features.

Key features in the dataset include:

*   **MSSubClass:** The building class
*   **MSZoning:** The general zoning classification
*   **LotArea:** Lot size in square feet
*   **LotConfig:** Lot configuration
*   **BldgType:** Type of dwelling
*   **OverallCond:** Overall condition rating
*   **YearBuilt:** Original construction date
*   **YearRemodAdd:** Remodel date
*   **Exterior1st:** Exterior covering on house
*   **BsmtFinSF2:** Type 2 finished square feet
*   **TotalBsmtSF:** Total basement square feet
*   **SalePrice:** The property's sale price (target variable)

### Steps Performed

1.  **Data Loading:** The House Price Prediction dataset was loaded from a CSV file (`HousePricePrediction.csv`) into a Pandas DataFrame.
2.  **Data Inspection:**

    *   The first few rows of the dataset were displayed to get a sense of the data.
    *   Descriptive statistics (mean, median, standard deviation, etc.) were calculated for each numerical feature to understand their distributions.
    *   The data types of each column were checked to ensure they were appropriate.
    *   Checked the number of rows and columns in the dataset.
3.  **Data Cleaning:**

    *   Checked for missing values using `.isnull().sum()`. Missing values were handled appropriately (dropping the target variable with missing values).
    *   Removed any unnecessary columns (e.g., 'Id').
4.  **Feature Engineering:**

    *   Converted categorical features into numerical using one-hot encoding with `pd.get_dummies()`.
    *   Handled multicollinearity and dimensionality reduction via correlation analysis
5.  **Data Scaling:**

    *   Scaled the numerical features using `MinMaxScaler` to ensure all features are on the same scale.
6.  **Model Training and Evaluation:**

    *   Split the data into training and testing sets.
    *   Trained a Linear Regression model on the training data.
    *   Evaluated the model's performance on the testing data using Mean Absolute Error (MAE).

### Tools Used

*   Python
*   Pandas
*   NumPy
*   Seaborn
*   Matplotlib
*   Scikit-learn (sklearn)

### Key Findings and Insights

*   One-hot encoding of categorical variables significantly expands the feature space.
*   Scaling numerical features improves the performance and stability of linear regression models.
*   The linear regression model achieved a sure MAE, indicating the average absolute difference between predicted and actual sale prices. 
*   The Lasso Regression model was added to reduce the impact of less relevant features on the overall model and provided an improved MAE value.

### Model Performance

*   **Linear Regression MAE: 0.04

### Conclusion

This project demonstrated the building of a linear regression model to predict house prices. Data preprocessing, feature engineering, and data scaling were crucial to improving model performance. The model can be further enhanced by exploring other regression algorithms, feature selection techniques, and hyperparameter tuning.  Also, it is crucial to consider the impact of missing data the importance of investigating missingness, and the potential introduction of bias that the missingness implies.
dimensions. Petal length and petal width are beneficial for distinguishing between species, while sepal measurements are less discriminatory. The strong correlation between petal length and width suggests that these features are related and could be used together in predictive models. The insights gained from this EDA can inform the selection of appropriate features and models for classification tasks involving the Iris dataset. Further analysis could include building machine learning models to predict Iris species based on these measurements.


