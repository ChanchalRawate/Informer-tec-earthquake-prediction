# 🌎 Informer-based TEC Earthquake Anomaly Detection

## 🔍 Overview
This project uses an **Informer deep learning model** to detect **ionospheric anomalies** in **Total Electron Content (TEC)** data that may indicate **pre-earthquake signals**.  
The model learns temporal dependencies in TEC variations to identify unusual disturbances before seismic events.

---

## 🧠 Model Architecture
- **Model Type:** Informer (Transformer-based time series model)
- **Input Features:** Solar and geomagnetic indices (`f107`, `ap`), time-based parameters (`DOY`, `HOD`), and delayed TEC values  
- **Output:** Predicted TEC value for the next time step  
- **Loss Function:** Mean Squared Error (MSE)  
- **Optimizer:** Adam (`lr=1e-5`, `eps=1e-8`)

---

## 📊 Model Evaluation Metrics
| Metric | Value |
|--------|--------|
| **Mean Absolute Error (MAE)** | 2.8708 |
| **Root Mean Square Error (RMSE)** | 3.8958 |

---

## ⚠️ Anomaly Detection
After training, residual analysis was applied to identify anomalous points where:
\[
|Z| > 2.5
\]
Detected **20 potential ionospheric anomalies** that may be **precursors to earthquakes**.

---

## 📈 Sample Output
![Model Evaluation Graph](https://raw.githubusercontent.com/ChanchalRawate/Informer-tec-earthquake-prediction/main/model_evaluation_plot.png)
![Anomaly Detection Graph](https://raw.githubusercontent.com/ChanchalRawate/Informer-tec-earthquake-prediction/main/anomaly_detection_sample.png)



---

## ⚙️ How to Run in Colab
1. Open this notebook directly in Google Colab:
   - Click on the notebook file in GitHub  
   - Then click **“Open in Colab”**
2. Run all cells — training, evaluation, and anomaly detection will execute automatically.

---

## 👩‍💻 Author
**Chanchal Rawate**  
Earthquake Ionospheric Anomaly Detection using Informer Model  
📅 2025
