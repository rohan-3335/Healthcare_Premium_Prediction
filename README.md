# Health Insurance Cost Predictor

This project is a health insurance premium prediction application built using machine learning and deployed with Streamlit. The model estimates insurance costs based on user inputs like age, income, medical history, and lifestyle.

## Project Overview

The Health Insurance Cost Predictor leverages a trained machine learning model to estimate insurance premiums, taking into account factors such as:
- Demographics (age, gender, marital status, region)
- Health and lifestyle (smoking status, BMI category, medical conditions)
- Employment and income details

The application comprises:
- A machine learning model trained with Scikit-Learn and XGBoost, handling predictions for both young and general populations.
- A helper module to preprocess inputs, normalize risk, and apply scaling.
- A user interface built with Streamlit to collect inputs and display predictions.

## File Structure

- **prediction_helper.py**: This script includes functions for data preprocessing, calculating risk scores, handling scaling, and generating predictions based on user input.
- **main.py**: The main application file, built with Streamlit, to create the user interface. It collects user input, interacts with the prediction helper, and displays the insurance cost estimate.
- **artifacts/**: Directory containing saved machine learning models and scaler objects for different age groups.
- **requirements.txt**: Lists all the dependencies required to run the project.

## How It Works

1. **Preprocessing Inputs**: The `preprocess_input()` function encodes and scales user inputs to make them model-ready.
2. **Risk Score Normalization**: A normalized risk score is calculated based on the user's medical history.
3. **Prediction Generation**: Based on the user's age, the appropriate model is used to make predictions for younger and older demographics.
4. **User Interaction**: The Streamlit app provides a form where users enter details and view predicted health insurance costs.

## Getting Started

### Prerequisites

Install the necessary packages:
```bash
pip install -r requirements.txt
