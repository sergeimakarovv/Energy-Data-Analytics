# Energy Data Analytics

### **Description:**

The project objective is to analyze global energy data, derive meaningful insights from it and visualize findings in a comprehensible format. In addition, a Streamlit app with an interactive dashboard was created and deployed, and also by using Machine Learning several models of predicting CO2 emissions were trained and evaluated.

You can find the dataset on [**Kaggle**](https://www.kaggle.com/datasets/anshtanwar/global-data-on-sustainable-energy) with a detailed description.

[![Earth-energy.png](https://i.postimg.cc/YSGdhW2k/Earth-energy.png)](https://postimg.cc/f3scPk0g)

### **Python libraries used:** 

- pandas: data cleaning and transformation
- plotly: visualizing data, creating various charts
- scikit-learn: ML models and evaluation metrics
- streamlit: creating an online dashboard

## **Project overview**

**1. Data cleaning and transformation**

Checking the dataset for missing values and duplicates, shortening column names and adding new derived columns.

**2. Exploratory Data Analysis**

Answering questions regaring the dataset by using data transformation and filtering, and creating various types of charts: 

- Top 10 countries by the amount of electricity generated from renewable sources
- Correlation matrix of all numerical variables
- Distribution of renewable energy share in countries on each continent
- CO2 emissions per capita vs. GDP per capita
- Distribution of the amount of renewable energy produced in European Union
- Dynamics of electricity generation in the European Union
- Energy intensity level of primary energy vs. renewable energy share in power generation in the EU

After that, the relevant dataset is downloaded in order to be used for the Streamlit dashboard.

**3. Machine Learning - Predicting CO2 emissions**

- **Pre-processing data**: dropping irrelevant columns, removing rows with missing values and duplicates, encoding categorical data into numeric.
- **Feature Engineering**: calculating features' correlations with the target variable and removing irrelevant ones, dropping some features that highly correlate with each other to avoid multicollinearity.
- **Modeling**: splitting the data into training and testing sets, scaling the features, creating and evaluating machine learning models.

5 different Machine Learning models are trained: *Linear Regression, Random Forest Regression, Gradient Boosting Regression, K Neighbors Regression, XGBoost Regression*. The models are evaluated by several metrics: *median absolute error, mean absolute error, mean squared error, root mean squared error, coefficient of determination*.

Based on the evaluation metrics, Random Forest Regression outperformed others and demonstrated the lowest error and the highest prediction accuracy.

**4. Streamlit Dashboard**

Creating an interactive dashboard with:

- Slider and checkbox filter with the options to choose a particular year, continent and type of energy
- Colored map representing the amount of electricity generation in each country for a selected year
- Pie chart with the energy distribution for a selected continent
- Bar chart illustrating top 5 energy producers for a selected continent and year
- Button to download the filtered dataset

## **Notes**

How to run the code:

- Ensure to download the necessary packages as in `requirements.txt`
- Download the dataset `global-data-on-sustainable-energy.csv` from Kaggle
- In case you change the file name, also change the data path in the code `pd.read_csv('<YOUR DATA PATH>')`
- Download the processed dataset for the dashboard
- Run the Streamlit dashboard by typing `streamlit run energy_dashboard.py` on the terminal


