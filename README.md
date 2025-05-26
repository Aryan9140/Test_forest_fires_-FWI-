
# 🔥 FWI Prediction Web App

This is a machine learning-powered **Flask web application** that predicts the **Fire Weather Index (FWI)**. It uses a trained **Ridge Regression** model and a **StandardScaler** to provide fire risk predictions based on user input.

## 📌 Features

- Predicts FWI based on:
  - Temperature
  - Relative Humidity
  - Wind Speed
  - Rain
  - FFMC
  - DMC
  - ISI
  - Region
  - Classes
- Clean and user-friendly form in HTML
- Powered by Flask
- Machine Learning model trained offline
- Realtime prediction using model and scaler saved in `.pkl` format

---

## 📁 Project Structure

MACHINE_LEARNING-PROJECT/
│
├── app.py # Main Flask app file
├── models/
│ ├── ridge.pkl # Trained Ridge Regression model
│ └── scaler.pkl # StandardScaler for input data
│
├── templates/
│ ├── index.html # Form input page
│ └── home.html # Prediction result page
│
├── static/ # (Optional) Static CSS/JS files
│
├── requirements.txt # Python dependencies
├── README.md # Project documentation
└── .gitignore # Git ignore file



🧠 How It Works
The user enters data like temperature, wind speed, and humidity in a web form.

Flask receives the form data, standardizes it using scaler.pkl.

The standardized data is passed to the trained ridge.pkl model.

The model predicts the FWI value and shows it on the result page.

📝 Input Fields in Form
Field	Description
Temperature	Temperature in °C
RH	Relative Humidity (%)
WS	Wind Speed (km/h)
Rain	Rainfall in mm
FFMC	Fine Fuel Moisture Code
DMC	Duff Moisture Code
ISI	Initial Spread Index
Classes	Fire class type (A, B, etc.)
Region	Region name/number

💻 Technologies Used
Python 3

Flask

scikit-learn

HTML/CSS

Jinja2 templates

Pickle for saving models

📦 requirements.txt Example
txt
Copy code
flask
numpy
pandas
scikit-learn
✅ TODO / Future Enhancements
Add deployment using Render/Railway

Add support for CSV upload

Improve UI with CSS or Bootstrap

Add model confidence or risk levels
