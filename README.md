# Rain Prediction

### Rain Prediction in Australia
This project develops a binary classification model to predict the occurrence of rain the following day across various Australian locations. By analyzing meteorological data such as temperature, humidity, and wind speed, the model provides an automated way to forecast precipitation.

### Dataset

The project uses the Weather dataset from the Rattle package.
Size: 145,460 entries with 23 initial features.
Target Variable: RainTomorrow (Yes/No).
Key Features: Minimum/Maximum temperature, Rainfall, Wind Gust Speed, Humidity at 9am/3pm, and Atmospheric Pressure.

Link to the dataset: https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package

Data Preprocessing

To prepare the raw weather data for machine learning, the following steps were taken:

Feature Selection: Dropped columns with excessive missing values or low analytical relevance, including Evaporation, Sunshine, Cloud9am, Cloud3pm, Location, and Date.

Handling Missing Values: Removed remaining rows with null values to ensure a clean dataset for training.

Categorical Encoding: Converted categorical variables (like RainToday and WindDir) into numerical formats using LabelEncoder.

Normalization: Used StandardScaler to rescale numerical features, ensuring that variables with different units (e.g., Pressure vs. Temp) contribute equally to the model.

### Model Architecture and Training

The following machine learning algorithms were implemented to predict whether it will rain the next day:

1. Logistic Regression: Used as a baseline classification model. It is a linear model that estimates the probability of a binary response (Rain/No Rain) based on one or more predictor variables.

2. Decision Tree Classifier: A non-parametric supervised learning method. It was used to create a model that predicts the value of the target variable by learning simple decision rules inferred from the weather data features.

3. Random Forest Classifier: An ensemble learning method that operates by constructing a multitude of decision trees at training time. It was used to improve predictive accuracy and control over-fitting, which is common with individual decision trees.

4. XGBoost Classifier (Extreme Gradient Boosting): A high-performance implementation of gradient boosted decision trees. This was used as the advanced model in the notebook, optimized for speed and performance, and it typically yielded the best results among the group.

### Performance Comparison
The models were evaluated using Accuracy, Precision, Recall, and F1-Score.

### Technologies Used
Python 3

Pandas & NumPy: For data manipulation.

Matplotlib & Seaborn: For exploratory data visualization.

Scikit-Learn: For preprocessing and Random Forest implementation.

XGBoost: For the final high-performance gradient boosted model.

### How To Run
1. Install Dependencies
   ```Bash
   pip install pandas numpy seaborn matplotlib scikit-learn xgboost
   ```
2. Open the notebook
   Launch rain-prediction.ipynb in Jupyter or VS Code to view the full data cleaning and modeling pipeline.
