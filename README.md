# Prescripto - Medical Symptom Analyzer

A web application that uses machine learning to analyze symptoms and provide information about potential diseases, treatment options, medications, diet recommendations, and exercise advice.

## 📋 Overview

Prescripto is a Flask-based web application that allows users to enter their symptoms and receive:

- 🩺 **AI-powered disease prediction** for common ailments
- 📖 **Detailed descriptions** of the predicted conditions
- 💊 **Recommended medications** specific to the diagnosed condition
- 🥗 **Diet recommendations** to support recovery and health
- 🏋️ **Exercise advice** tailored to the condition
- 🛡️ **Precautionary measures** to prevent complications

The application leverages a trained SVC (Support Vector Classification) model to analyze user-input symptoms and generate appropriate medical predictions.

## ⚠️ Important Disclaimer

> **This application is intended for educational and informational purposes only.**  
It is **not a substitute for professional medical advice, diagnosis, or treatment**. Always seek guidance from a qualified healthcare provider for medical concerns.

## 🚀 Features

- 💡 Clean, responsive UI with **Light/Dark mode toggle**
- 🤖 **Machine learning-powered** symptom analysis using SVC model
- 📋 Structured results: **disease prediction, description, medications, diet, workouts, precautions**
- 📱 **Mobile-friendly** design with **Tailwind CSS**
- 🔍 **Interactive symptom selector** with search functionality
- 🏷️ **Tag-based UI** for selecting multiple symptoms
- 🌙 **Dark mode support** for comfortable viewing in low-light environments

## 🔧 Installation

1. **Clone the repository:**
   ```bash
    git clone https://github.com/mohitooo28/prescripto_ml.git
    cd prescripto-ml
   ```


2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv

   # On Windows
   venv\Scripts\activate

   # On macOS/Linux
   source venv/bin/activate
   ```


3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🏃‍♂️ Running the Application

```bash
# Run the Flask application
python main.py
```

The application will be available at http://localhost:5000/

## 💻 Usage

- Select your **symptoms** using the interactive dropdown menu
- Multiple symptoms can be selected by clicking on them in the dropdown list
- Selected symptoms appear as tags that can be removed if needed
- Click the **"Predict"** button to analyze your symptoms
- View ML-generated:
  - Disease prediction
  - Detailed description
  - Recommended precautions
  - Suggested medications
  - Recommended diet plan
  - Appropriate exercise recommendations
- Click **"Clear"** to reset the form and start over

## 🛠️ Tech Stack

- **Backend**: Python, Flask
- **Frontend**: HTML, JavaScript, Tailwind CSS
- **Machine Learning**: scikit-learn (SVC model)
- **Data Processing**: NumPy, Pandas
- **Model Serialization**: pickle

## 📊 ML Model Information

The application uses a Support Vector Classifier (SVC) trained on a dataset of symptoms and their corresponding diseases. The model:

- Supports identification of 41 different diseases
- Processes 132 different symptoms
- Provides high accuracy prediction based on symptom combinations
- Was trained on a comprehensive medical dataset

## 📁 Project Structure

```
prescripto/
├── dataset/               # Contains all the medical data files
│   ├── description.csv    # Disease descriptions
│   ├── diets.csv          # Diet recommendations
│   ├── medications.csv    # Medication information
│   ├── precautions_df.csv # Precautionary measures
│   ├── symtoms_df.csv     # Symptoms dataset
│   ├── Training.csv       # Training data for the ML model
│   └── workout_df.csv     # Exercise recommendations
├── model/                 # Contains trained ML models
│   ├── rf.pkl             # Random Forest model
│   └── svc.pkl            # Support Vector Classifier model
├── static/                # Static files (CSS, images, etc.)
├── templates/             # HTML templates
│   ├── about.html
│   ├── blog.html
│   ├── contact.html
│   ├── developer.html
│   └── index.html         # Main application page
├── main.py                # Flask application entry point
├── medical recommendation system.ipynb  # Jupyter notebook for model training
└── requirements.txt       # Project dependencies
```

## 🧠 Machine Learning Pipeline

1. **Data Preprocessing**: Converting symptoms to numerical features
2. **Model Training**: Using SVC with linear kernel
3. **Prediction**: Converting user symptoms to feature vectors
4. **Post-processing**: Retrieving disease information, precautions, medications, diet, and workout recommendations

## 📌 Acknowledgments

- 🧪 **scikit-learn** for the machine learning tools
- 🐍 **Flask** for the web framework
- 🎨 **Tailwind CSS** for the sleek and responsive design
- 📊 The creators of the medical datasets used to train the models
