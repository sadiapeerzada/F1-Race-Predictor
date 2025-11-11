# 🏎️ F1 Race Predictor  

A **Machine Learning–based web application** that predicts **Formula 1 race outcomes** using historical data, track details, and weather conditions.  
Built with **Python**, **Scikit-learn**, **Pandas**, and **Streamlit**, this project blends data science with sports analytics to forecast race winners and podium probabilities.  

---

## 🌟 Introduction  

Formula 1 is a sport of **speed, precision, and strategy** — where every lap, weather condition, and starting position can make or break a driver’s race.  

The **F1 Race Predictor** leverages historical data to analyze race trends and predict possible outcomes.  
It provides an **interactive dashboard** where users can input race parameters (track, weather, grid position, etc.) and instantly receive predictions and visual analytics.  

This project demonstrates how **machine learning models** can be applied to **sports analytics**, offering engaging, data-driven insights into racing dynamics.  

---

## 🧰 Features  

- 🧠 **Race Winner Prediction:** Predicts the most likely winner using a trained Random Forest model.  
- 🥇 **Top 3 Podium Forecast:** Shows probabilities for the top 3 finishers.  
- 🌦️ **Weather Sensitivity:** Adapts predictions based on wet/dry track conditions.  
- 🧮 **Custom Input Fields:** Select your track, weather, and grid position dynamically.  
- 📊 **Data Visualization:** Displays charts such as driver performance trends and feature importance.  
- 💾 **Reusable Model:** Save and reload the model (`f1_model.pkl`) for fast predictions.  

---

## ⚙️ Installation & Setup  

Follow these steps to set up the project locally on your system:  

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/f1-race-predictor.git
cd f1-race-predictor
```
## ⚙️ 2️⃣ Install Dependencies

Install all required libraries listed in **`requirements.txt`**:

```bash
pip install -r requirements.txt
```
## 🧩 Core Dependencies

| Library | Purpose |
|----------|----------|
| **pandas** | Data handling and manipulation |
| **numpy** | Numerical computation |
| **scikit-learn** | Machine learning algorithms |
| **streamlit** | Web app framework |
| **matplotlib** | Data visualization |

---

## 🛠️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/sadiapeerzada/F1-Race-Predictor.git
cd F1-Race-Predictor
## 2️⃣ Install Dependencies
bash
pip install -r requirements.txt
```
## 3️⃣ Prepare the Dataset
Upload your F1 dataset ZIP file into the dataset/ folder.
Unzip the file in place, ensuring that all CSVs are inside.

## 🗂️ Example Directory Structure
```bash
dataset/
│
├── f1_race_results.csv
├── drivers.csv
├── constructors.csv
└── weather_data.csv
```
----
📁 The model expects features such as driver, constructor, grid position, track, weather, and finishing position.

## 🤖 4️⃣ Train the Model (Optional)
Run the following command to train your model:
```bash
python model.py
This step will:
```

## ✅ Preprocess historical data

+ 🔠 Encode categorical features (driver, constructor, etc.)

+ 🌳 Train a Random Forest Classifier

+ 💾 Save the trained model as f1_model.pkl

+ 💡 Tip: If f1_model.pkl already exists, you can skip this step.

----

## 🖥️ 5️⃣ Run the Streamlit App
Launch the interactive app using:
```bash
streamlit run app.py
Once running, you can:


Select Track, Weather, and Grid Position

Click Predict Winner

View predictions for the winner and podium finishers
```
## 🧠 How It Works

## 🔹 Data Preprocessing
+ Loads CSV data using pandas

+ Handles missing values and performs cleaning

+ Encodes categorical columns using LabelEncoder / OneHotEncoder

+ Normalizes numerical features like grid position and laps

## 🔹 Model Training
+ Uses Random Forest Classifier from scikit-learn

+ Splits dataset into 80:20 train-test ratio

+ Learns race outcome probabilities

+ Optionally supports regression for lap time prediction

## 🔹 Model Evaluation
+ Evaluated using accuracy, precision, and confusion matrix

+ Feature importance plotted for interpretability

## 🔹 Model Saving
+ Trained model is serialized as f1_model.pkl using pickle

+ Enables fast inference without retraining

----

## 💻 Streamlit Interface
The Streamlit app (app.py) serves as the web-based interface for predictions.

## ✨ Features
Dropdowns for selecting Track, Weather, and Grid Position

“Predict Winner” button triggers model inference

Displays top 3 podium predictions with probabilities

Optionally visualizes feature importance and historical charts

---
## 🏎️ Example Layout

```bash

 🏎️ F1 Race Predictor
------------------------------------
Select Track:     [Monza]
Select Weather:   [Dry]
Select Grid Pos:  [5]

[PREDICT WINNER]

Predicted Winner: Lewis Hamilton  
Podium:

1️⃣ Hamilton (0.62)  
2️⃣ Verstappen (0.29)  
3️⃣ Leclerc (0.09)
📊 Example Output
Input	Predicted Winner	Podium (Top 3)
Track: Monza
Weather: Dry

Grid: 5	🥇 Lewis Hamilton	1️⃣ Hamilton
2️⃣ Verstappen
3️⃣ Leclerc
Track: Silverstone
Weather: Rain

Grid: 10	🥇 Max Verstappen	1️⃣ Verstappen
2️⃣ Hamilton
3️⃣ Leclerc
```

## 🧱 Project Architecture
```bash
f1-race-predictor/
│
├── dataset/                     # Raw and processed data files
│   ├── f1_race_results.csv
│   ├── drivers.csv
│   ├── constructors.csv
│   └── weather_data.csv
│
├── model.py                     # Handles preprocessing and model training
├── app.py                       # Streamlit web interface
├── f1_model.pkl                 # Saved ML model
├── requirements.txt             # Python dependencies
├── README.md                    # Documentation
└── assets/                      # Images, charts, or GIFs for README
    ├── demo_screenshot.png
    └── feature_importance.png

```

## 🧩 Technologies Used

Category	Technology
Programming Language	Python
Machine Learning	Scikit-learn
Data Handling	Pandas, NumPy
Visualization	Matplotlib
Web Framework	Streamlit
Model Storage	Pickle
Data Sources	Ergast API, Kaggle F1 Datasets

---

## 🚀 Future Enhancements
🔄 What-if Simulations: Test hypothetical weather or grid scenarios

🧮 Lap Time Prediction: Predict per-driver lap times

🌐 Live Data Integration: Connect with real-time F1 APIs

🏁 Championship Forecasting: Simulate entire seasons

🗺️ Interactive Visuals: Add track maps & telemetry dashboards

## 📚 Data Sources
Ergast F1 API — Official F1 race data and metadata

Kaggle F1 Datasets — Historical qualifying, lap, and race data

---
## 🧾 License

This project is licensed under the MIT License — free for personal and educational use.
See the LICENSE file for details.

---

## 🏁 Final Notes
The F1 Race Predictor is more than just a prediction tool — it’s a data science showcase combining racing passion with machine intelligence.
It demonstrates how historical data, feature engineering, and machine learning can work together to forecast outcomes in one of the most unpredictable sports.

“Data is the new fuel — and in Formula 1, it drives everything from the car to the code.” 🏎️💨

