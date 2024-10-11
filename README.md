# Crop-Product Export Value Prediction

## Overview

This project aims to forecast the export value of crop products for a specific geographical region up to three years into the future. The prediction model is built using a Multilayer Perceptron (MLP) neural network. The following steps are carried out to preprocess the data, engineer features, and train the model:

### Key Features:
- **Data Preprocessing**: Cleaning, normalization, and handling missing values.
- **Data Integration**: Merging 13 datasets related to food and agriculture into a single comprehensive dataframe.
- **Feature Engineering**: Creating lag features, normalizing data, and encoding categorical variables to enhance model performance.
- **Modeling**: Building an MLP model to predict the export value of crop products three years into the future.

## Data Preprocessing

The raw data consisted of multiple CSV files with various categories of variables related to food and agriculture. Data preprocessing was carried out as follows:

- **Data Loading**: Each CSV file was loaded into a pandas dataframe for examination and further processing.
- **Cleaning**: Unnecessary columns were dropped, and missing values were handled appropriately.
- **Merging**: The datasets were merged on the common columns of `Country` and `Year`, ensuring that all relevant features were aligned.

## Feature Engineering

Several important features were engineered to improve the model's predictive power:

- **Lag Features**: Lag features for export value were created, including export values from 1, 2, and 3 years prior.
- **Normalization**: A RobustScaler was applied to normalize the features, improving the stability of the model.
- **Encoding**: Categorical variables, such as country and product type, were label encoded to allow the model to process them effectively.

## DataFrame Structure

The final dataframe used for modeling contains the following features:

- **Year**: The year the data was recorded.
- **Country (Area)**: Encoded representation of the country.
- **Products**: Encoded product types.
- **Exchange Rate**: Average exchange rate for the given year.
- **Land Temperature**: Average annual land temperature in the region.
- **Export Value Lag1**: Export value from one year prior.
- **Export Value Lag2**: Export value from two years prior.
- **Export Value Lag3**: Export value from three years prior.

## Model

The project uses a **Multilayer Perceptron (MLP)** to predict the export value of crop products. The model is trained on historical data and attempts to forecast the export value up to three years in advance.

### Model Parameters:
- **Input Features**: All the features described above, including the lag features and external factors like exchange rate and temperature.
- **Target Variable**: Export value of crop products.

## How to Use

### Prerequisites:
- Python 3.x
- Libraries: `pandas`, `numpy`, `scikit-learn`, `tensorflow` (or `keras`), `matplotlib`

### Running the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/crop-product-prediction.git
