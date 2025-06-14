# House Price Prediction: Regression with the Ames Dataset

This project focuses on predicting home sale prices using the Ames Housing dataset, provided in the "House Prices - Advanced Regression Techniques" Kaggle competition. The main idea was to explore different regression techniques to build a model that could accurately estimate property prices.

## Project Steps

The process was divided into four main parts:

1.  **Data Loading and Exploratory Data Analysis (EDA)**:
    * The training (`train.csv`) and testing (`test.csv`) datasets were loaded using Pandas.
    * The `data_description.txt` file was consulted to understand the 79 explanatory variables.
    * Visualizations with Matplotlib and Seaborn helped in understanding distributions, missing values, outliers, and correlations with the sale price (SalePrice).

2.  **Preprocessing and Feature Engineering**:
    * Missing values were handled with specific strategies for each data type.
    * Categorical variables were transformed into numerical values using techniques like one-hot encoding and label encoding.
    * Some new *features* were also created to improve the model, such as a variable that combines the construction year with the renovation year to represent the "real age" of the house.

3.  **Model Selection, Training, and Evaluation**:
    * Random Forest was used as the regression model, along with the TensorFlow and Yggdrasil Decision Forests libraries.
    * The training set (`train.csv`) was used to train the models. Techniques like cross-validation helped evaluate model performance and tune hyperparameters.

4.  **Generating Predictions and Submission**:
    * The same preprocessing was applied to the test data.
    * The final model generated the `SalePrice` predictions, which were saved to the file.
    * The metric used for evaluation was RMSLE (Root Mean Squared Logarithmic Error), as per the competition rules.

## Results

* The trained model was able to predict prices with a good margin of accuracy, considering the available variables. It achieved a score of 0.14857 in the Kaggle competition.
* The predictions were consolidated in `submission.csv`.
* The `code.ipynb` notebook contains the entire workflow, from data import to the generation of final predictions.

## Technologies Used

* **Python**: The main programming language.
* **Pandas**: For data manipulation and analysis.
* **NumPy**: For numerical operations.
* **Scikit-learn**: For preprocessing, implementation of models (like Random Forest), and evaluation metrics.
* **Matplotlib & Seaborn**: For data visualization.
* **TensorFlow & Yggdrasil Decision Forests (`ydf`)**: Libraries for building and training advanced machine learning models.

## Possible Next Steps

* Test more creative feature creation approaches.
* Better optimize hyperparameters with techniques like Grid Search, Random Search, or even Bayesian Optimization.
* Explore more sophisticated ensemble models.
* Analyze the model's errors to understand where it can be improved.

---

## Citations

* **Kaggle Competition:**
    Anna Montoya and DataCanary. House Prices - Advanced Regression Techniques. [https://kaggle.com/competitions/house-prices-advanced-regression-techniques](https://kaggle.com/competitions/house-prices-advanced-regression-techniques), 2016. Kaggle.

* **Ames Housing Dataset:**
    The Ames Housing dataset was compiled by Dean De Cock for use in data science education. It is a modern and expanded alternative to the frequently used Boston Housing dataset.
