# HexSoftwares_Project_Exploratory-Data-Analysis.

## Project Overview

This project performs Exploratory Data Analysis (EDA) on the Iris dataset, a classic dataset in machine learning and statistics. The dataset contains 150 instances of iris flowers, with measurements of their sepal length, sepal width, petal length, and petal width (all in centimeters). This EDA aims to understand the underlying structure of the data, identify potential relationships between features, and gain insights into how these features differentiate the three Iris species: Setosa, Versicolor, and Virginica.

## Dataset Information

The Iris dataset includes the following features:

*   **Id:** A unique identifier for each flower sample.
*   **SepalLengthCm:** Length of the sepal in centimeters.
*   **SepalWidthCm:** Width of the sepal in centimeters.
*   **PetalLengthCm:** Length of the petal in centimeters.
*   **PetalWidthCm:** Width of the petal in centimeters.
*   **Species:** The species of the iris flower (Setosa, Versicolor, or Virginica).

## Steps Performed

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

## Tools Used

*   Python
*   Pandas
*   NumPy
*   Matplotlib
*   Seaborn

## Key Findings and Insights

*   **Species Differentiation:** The Iris species can be relatively well separated using petal measurements (length and width). Setosa is particularly distinct from Versicolor and Virginica.
*   **Feature Correlations:**
    *   Strong positive correlations exist between petal length and petal width. This suggests that as petal length increases, petal width tends to increase as well.
    *   Sepal length and sepal width show a weaker correlation compared to petal dimensions.
*   **Data Distributions:**
    *   Petal length and petal width exhibit apparent differences across the three species, making them good candidates for classification.
    *   Sepal width has more overlap between the species, making it a less reliable feature for distinguishing between them.
*   **Outliers:**
    *   Box plots revealed some outliers in sepal width, indicating some flowers with unusually large or small sepal widths compared to the rest of the dataset.
*   **Observations on Species:**
    *   *Iris setosa* tends to have smaller petal lengths and widths but larger sepal widths.
    *   *Iris virginica* tends to have larger petal lengths and widths but smaller sepal widths.
    *   *Iris versicolor* falls in between *Iris setosa* and *Iris virginica* in terms of petal and sepal dimensions.

## Visualizations

*   **Pairplot:**  Illustrates the relationships between all pairs of features, with different colors representing different species.

    (Ideally, you would embed the pairplot image here)

*   **Correlation Heatmap:**  Displays the correlation coefficients between numerical features.  Darker colors indicate stronger correlations (positive or negative).

    (Ideally, you would embed the heatmap image here)

## Conclusion

The Exploratory Data Analysis of the Iris dataset revealed significant insights into the characteristics of the different Iris species and the relationships between their sepal and petal dimensions. Petal length and petal width are beneficial for distinguishing between species, while sepal measurements are less discriminatory. The strong correlation between petal length and width suggests that these features are related and could be used together in predictive models. The insights gained from this EDA can inform the selection of appropriate features and models for classification tasks involving the Iris dataset. Further analysis could include building machine learning models to predict Iris species based on these measurements.


