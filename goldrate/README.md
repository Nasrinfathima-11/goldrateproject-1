Gold Rate Prediction in India 🇮🇳

📌 Project Overview

This project predicts the gold rate in India using a Machine Learning regression model. It uses Gradio to provide a simple web interface where users can enter the USD to INR exchange rate and get a predicted gold rate.

The project uses a pre-trained regression model and a scaler to process the input and generate predictions.

🚀 Features

Predicts the gold rate using a trained Machine Learning model.

Uses a scaler to transform input data before prediction.

Provides an interactive web interface using Gradio.

Displays the predicted value rounded to two decimal places.

Can generate a publicly accessible demo link using Gradio's sharing feature.

🛠️ Technologies Used

Python – Programming language

Gradio – Web interface

NumPy – Numerical operations

Scikit-learn – Machine Learning preprocessing and prediction

Pickle – Loading the saved model and scaler

📂 Project Structure

Gold-Rate-Prediction/
│
├── app.py
├── regressor.pkl
├── scaler.pkl
└── README.md

File descriptions:

app.py – Main Python application.

regressor.pkl – Saved regression model.

scaler.pkl – Saved scaler used to preprocess input data.

README.md – Project documentation.

📦 Installation

1. Install Python

Install Python if it is not already installed on your computer.

2. Clone the Repository

git clone <your-repository-url>

Navigate to the project directory:

cd Gold-Rate-Prediction

3. Install Dependencies

Run the following command:

pip install gradio scikit-learn numpy

▶️ How to Run the Project

Make sure app.py, regressor.pkl, and scaler.pkl are in the same directory.

Run the application:

python app.py

Gradio will start the application and display a local URL in the terminal. Open that URL in your browser to use the prediction interface.

The application also uses share=True to create a public sharing link when supported.

💻 How It Works

The application loads the pre-trained regression model from regressor.pkl.

It loads the scaler from scaler.pkl.

The user enters a USD to INR exchange rate.

The scaler transforms the input into the format expected by the model.

The regression model predicts the output.

The predicted value is rounded to two decimal places and displayed on the interface.

🧠 Prediction Function

def calculate_goldrate(usd_inr):
    scaled_input = scaler.transform(
        np.array(usd_inr).reshape(1, -1)
    )
    prediction = model.predict(scaled_input)[0]
    return round(float(prediction.item()), 2)

⚠️ Important Notes

The trained model and scaler files must be available before running the application.

The input must use the same feature and units expected during model training.

The prediction is only as reliable as the training data and model.

Although the interface mentions the gold rate in India now, the application does not fetch live gold prices or exchange rates. It predicts an output from the input and the saved model.

Ensure that the model's target variable represents the intended gold price unit, such as INR per gram, before interpreting the result as the current 1-gram gold rate.

Do not load pickle files from untrusted sources because they can execute malicious code.

🔮 Future Improvements

Integrate a live USD to INR exchange-rate API.

Integrate a live gold-price API.

Display historical gold-price trends using charts.

Improve prediction accuracy with updated training data.

Deploy the application to a cloud platform.

👨‍💻 Author

Your Name

📄 License

This project is intended for educational and learning purposes. Add a suitable open-source license if you plan to distribute the project publicly.