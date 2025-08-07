# 🌦️ Deep Learning-Based Long-Term Weather Forecasting 


📌 Project Overview
This project leverages deep learning techniques (specifically Long Short-Term Memory, or LSTM) to perform long-term monthly weather forecasting using historical data from 8 meteorological stations across Saudi Arabia. The goal is to forecast critical climate variables for the next 20 years based on historical patterns from 1981–2024.

## 📂 Dataset Overview
Each station includes parameters such as:
- Total Annual Rainfall
- Relative Humidity
- Surface Pressure
- Temperature (°C)
- Monthly precipitation
- And more..
- Datasets of Saudia Arabia 8 Different stations 
https://drive.google.com/file/d/10YpUy4hrkflcZ1wjkPwauzZCsNOriaVE/view?usp=sharing, https://drive.google.com/file/d/17AnIN4S_POf43EznundaaXDRNG6cgMjK/view?usp=sharing, https://drive.google.com/file/d/17nUb7ofxEi9jZOM6E0thdi7iW317q9Bm/view?usp=sharing, https://drive.google.com/file/d/196_joJSCsBEPEDiybxhcS6XDlEXny8YI/view?usp=sharing, https://drive.google.com/file/d/1AfZdRjh7ES2ImVHDcsRS7f3SdyHBslPE/view?usp=sharing, https://drive.google.com/file/d/1FTNtc9do_yjW2mEHjJr57BUe-zEVQLpT/view?usp=sharing, https://drive.google.com/file/d/1YXeLZ9HQPH1Ak3L6eJigA6bMcrVy-erK/view?usp=sharing, https://drive.google.com/file/d/1eRE3Yg1v4Ma5zUivMENQtbFzpV31GtHo/view?usp=sharing, https://drive.google.com/file/d/1e_op2--laYPBcp1iRxYSKJw3TDciZkSD/view?usp=sharing, https://docs.google.com/spreadsheets/d/1iqlriSFe0T8HhLPDg5SsAHM56M4TRbMAtrJD9jaDcXQ/edit?usp=sharing
Data range: **1981 to 2024**
## 🧠 Model Architecture

- **Sequence Model**: LSTM (Long Short-Term Memory)
- **Framework**: TensorFlow / Keras
- **Architecture**:
  - Input: 20-year sequences of normalized features
  - Layers: 1 LSTM (64 units) + Dense output layer
- **Forecast Horizon**: 20 years (2025–2044)

---

## 🛠️ Workflow

1. **Mount Google Drive** and extract zipped dataset
2. **Read & clean** all 8 station `.csv` files
3. **Handle missing values** via mean imputation
4. **Combine all data horizontally** for multivariate time series
5. **Normalize** with `MinMaxScaler`
6. **Train/Test split** using sequences of 20 years
7. **Train LSTM** model on the data
8. **Evaluate** using MAE, MSE, RMSE, R²
9. **Predict future** 20 years for all variables
10. **Plot results** (past vs future) for selected parameters

---

## 📊 Metrics

Evaluated using unscaled predictions:
- **MAE** (Mean Absolute Error)
- **MSE** (Mean Squared Error)
- **RMSE** (Root Mean Squared Error)
- **R² Score**

Example metrics:
MAE = 0.2787
MSE = 0.0123
RMSE = 0.1109
R² = 0.9654

yaml
Copy
Edit

---

## 📈 Forecast Plots

Forecasts are plotted for:
- Total Annual Rainfall
- Relative Humidity
- Surface Pressure (kPa)
- Temperature (°C)

Each plot includes the last 20 years of actuals (2005–2024) vs predicted values (2025–2044).

---

## 📁 Directory Structure

📦Weather-Prediction/
┣ 📂data/
┃ ┗ 📄station_csv_files.csv
┣ 📄weather_forecasting_lstm.ipynb
┣ 📄README.md
┗ 📄requirements.txt

yaml
Copy
Edit

---

## 🔮 Future Improvements

- Train separate models for each station for localized forecasting
- Experiment with bidirectional LSTM, GRU, or Transformers
- Integrate external features like ENSO, sea surface temperatures, etc.
- Deploy model via Flask or Streamlit for real-time forecasting

---

## 📜 Citation

If you use this code or dataset, please cite the following:
 
> LSTM Model Implementation based on TensorFlow  
> Developed by Rimsha Ansar, 2025

---

## 🧑‍💻 Author

**Rimsha Ansar**  
Machine Learning Researcher | Climate Modeling Enthusiast
