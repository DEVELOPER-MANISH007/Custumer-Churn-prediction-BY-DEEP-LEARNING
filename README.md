# Customer Churn Prediction using Deep Learning

This project builds and deploys a customer churn prediction system using an Artificial Neural Network (ANN). It predicts whether a bank customer is likely to leave the service based on customer attributes such as age, balance, geography, gender, tenure, credit score, and account activity.

The application uses a trained TensorFlow/Keras model and a Streamlit interface for easy prediction input and results.

## Project Overview

Customer churn is one of the most important business metrics for banks and service providers. This project helps identify customers who are at risk of leaving so that proactive retention strategies can be designed.

The workflow includes:
- Data preprocessing and encoding
- Feature scaling
- Model training with a deep learning ANN
- Saving the trained model and preprocessing artifacts
- Loading the model in a real-time Streamlit prediction app

## Technologies Used

- Python
- TensorFlow / Keras
- Streamlit
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- TensorBoard

## Project Structure

```text
Custumer Churn prediction BY DEEP LEARNING/
├── app.py                     # Streamlit web application for prediction
├── Data/
│   └── Churn_Modelling.csv   # Dataset used for modeling
├── logs/
│   └── fit/
│       ├── train/
│       └── validation/
├── model.h5                  # Trained neural network model
├── scaler.pkl                # StandardScaler object for input scaling
├── encoder_geo.pkl           # Encoded geography label encoder
├── lable_encoder_gender.pkl  # Gender label encoder
├── experiments.ipynb         # Notebook for experimentation
├── prediction.ipynb          # Notebook for prediction-related exploration
├── Requirements.txt          # Python dependencies
├── .gitignore
├── given_code/               # Reference or original notebook/code examples
│   ├── app.py
│   ├── Churn_Modelling.csv
│   ├── experiments.ipynb
│   ├── hyperparametertuningann.ipynb
│   ├── model.h5
│   ├── prediction.ipynb
│   ├── requirements.txt
│   └── salaryregression.ipynb
└── README.md                 # Project documentation
```

## Main Files

- `app.py`  
  Runs the Streamlit front-end and loads the trained model to predict churn.

- `model.h5`  
  Saved trained deep learning model.

- `scaler.pkl`  
  Stores the preprocessing scaler used to scale input features.

- `encoder_geo.pkl` and `lable_encoder_gender.pkl`  
  Store encoding metadata for categorical variables.

- `Data/Churn_Modelling.csv`  
  Source dataset for customer churn analysis.

## Setup Instructions

1. Open a terminal in the project folder.
2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r Requirements.txt
```

## Run the Application

Start the web app with:

```bash
streamlit run app.py
```

Then open the local URL shown in the terminal, usually:

```text
http://localhost:8501
```

## How the App Works

The Streamlit app collects customer details from the user, such as:
- Geography
- Gender
- Age
- Balance
- Credit score
- Estimated salary
- Tenure
- Number of products
- Credit card status
- Active member status

It then preprocesses these values, scales them, and passes them into the trained ANN model. The app displays the predicted churn probability and a simple status:
- likely to churn
- not likely to churn

## Notes

- This project is designed for educational and practical machine learning demonstration.
- The model artifacts are already generated and saved in the project root.
- The `given_code` folder contains reference notebooks and supporting files from the original implementation.

## Future Improvements

Possible enhancements include:
- Hyperparameter tuning
- Better feature engineering
- Cross-validation and evaluation metrics
- Deploying the model to cloud or web hosting
- Add user authentication and reporting dashboard

## License

This project is intended for learning and academic/demo purposes.
