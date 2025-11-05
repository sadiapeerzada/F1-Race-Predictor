# F1-Race-Predictor
Predict F1 race winners and podiums using historical data and machine learning. Interactive Streamlit app with driver, constructor, and track analytics.
# 🏎️ F1 Race Outcome Predictor

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)](https://www.python.org/) 
[![Streamlit](https://img.shields.io/badge/Streamlit-App-red?logo=streamlit&logoColor=white)](https://streamlit.io/) 
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

Predict **F1 race winners and podium positions** using historical data and machine learning. Built with **Python**, **Scikit-learn**, and **Streamlit**, this app lets users **simulate upcoming races**, **analyze historical performance**, and see **predicted outcomes** through an interactive web interface.

---

## 🎯 Features

| Feature | Description |
|---------|-------------|
| 🏆 **Race Winner Prediction** | Predict the winner based on qualifying positions, track, weather, and driver/constructor stats. |
| 🎖️ **Podium Probabilities** | Shows likelihood of top 3 finishers. |
| 💻 **Interactive Dashboard** | Streamlit web interface for easy user input and visualization. |
| 📊 **Historical Stats** | Visualize past driver and constructor performance at selected tracks. |
| 🔧 **Feature Importance** | Understand which factors (grid position, weather, driver skill) most influence predictions. |
| ⚡ **Simulation Mode (Future)** | Simulate race outcomes with variable conditions. |

---

## 📸 Demo

![Demo GIF](assets/demo.gif)  
*Example: Predicting winner for Monza with dry weather and grid position 5.*

---

## 💻 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/f1-race-predictor.git
cd f1-race-predictor
2️⃣ Install Dependencies
bash
Copy code
pip install -r requirements.txt
Dependencies:
pandas, numpy, scikit-learn, streamlit, matplotlib

3️⃣ Prepare Dataset
Upload your F1 dataset ZIP to the dataset/ folder.

Unzip it inside the folder.

Ensure CSV files are accessible (e.g., f1_race_results.csv).

4️⃣ Train the Model (Optional)
bash
Copy code
python model.py
Preprocess data

Train a Random Forest Classifier

Save model as f1_model.pkl

If f1_model.pkl already exists, you can skip this step.

5️⃣ Run the Streamlit App
bash
Copy code
streamlit run app.py
Input race details: Track, Weather, Grid position

Click Predict Winner

View predicted winner and top 3 podium probabilities

📂 Project Structure
graphql
Copy code
f1-race-predictor/
│
├── dataset/                 # CSV files from F1 historical data
├── model.py                 # Data preprocessing & model training
├── app.py                   # Streamlit web interface
├── f1_model.pkl             # Saved trained model
├── requirements.txt         # Python dependencies
├── README.md
└── assets/                  # Screenshots / GIFs for README
⚙️ How It Works
Data Preprocessing

Load historical race data (CSV) using pandas

Encode categorical features: driver, constructor, track, weather

Select numeric features: grid position, laps, driver/constructor stats

Model Training

Random Forest Classifier predicts race winners

Optional regression model predicts lap times or finishing positions

Model saved using pickle for quick loading

Streamlit Interface

Users select race details

Model predicts winner and top 3 podium

Optional charts: historical stats, feature importance

📈 Example Output
Input	Predicted Winner	Podium
Track: Monza
Weather: Dry
Grid: 5	Lewis Hamilton	1) Hamilton
2) Verstappen
3) Leclerc
Track: Silverstone
Weather: Rain
Grid: 10	Max Verstappen	1) Verstappen
2) Hamilton
3) Leclerc

🚀 Future Improvements
Predict lap times for all drivers

Forecast championship standings

Simulation mode for “what-if” scenarios

Integration with live F1 API for real-time predictions

Enhanced dashboard with track maps and interactive charts

📚 Data Sources
Ergast F1 API – Official historical F1 data

Kaggle F1 Datasets – Race results, qualifying, lap times

📝 License
MIT License – Free for personal and educational use.
