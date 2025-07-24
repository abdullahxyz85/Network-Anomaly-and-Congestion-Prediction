# Network Anomaly and Congestion Prediction

## 📡 Overview

This project provides an interactive web application for **Network Anomaly Detection** and **Congestion Prediction** using machine learning. It enables users to upload network traffic data, detect unusual patterns (anomalies), and predict network congestion, all with intuitive visualizations and reports.

---

## 🚀 Features

- **Upload Network Traffic Data (CSV)**
- **Anomaly Detection** using Isolation Forest
- **Network Congestion Prediction**
- **Interactive Visualizations** (histograms, scatter plots, pie charts)
- **Detailed Reports** (confusion matrix, classification report)
- **User-friendly Streamlit UI**

---

## 🛠️ Technologies Used

- **Python 3**
- **Streamlit** (for web UI)
- **Pandas, NumPy** (data processing)
- **Plotly** (visualizations)
- **scikit-learn** (machine learning: Isolation Forest, preprocessing, metrics)

---

## 📂 Dataset Format

The app expects a CSV file with at least the following columns:

- `Time`: Timestamp of the packet/event
- `No.`: Packet number
- `Protocol`: Protocol type (e.g., TCP, UDP, etc.)
- `Length`: Packet length

---

## 🏗️ How It Works

1. **Upload Data**: User uploads a CSV file containing network traffic data.
2. **Preprocessing**: Data is cleaned, timestamps are parsed, and categorical features are encoded.
3. **Anomaly Detection**: The Isolation Forest algorithm identifies unusual patterns in the data.
4. **Visualization**: Results are shown as tables and interactive charts.
5. **Congestion Prediction**: The app predicts network congestion using machine learning and displays results with metrics and charts.

---

## 📊 Methodology

### Anomaly Detection

- **Algorithm**: Isolation Forest
- **Features Used**: Length, Encoded Protocol, Hour, Packet Number
- **Contamination**: 10% (assumes 10% of data may be anomalous)
- **Output**: Each record is labeled as 'Normal' or 'Anomaly'.

### Congestion Prediction

- **Algorithm**: Isolation Forest (for demo; can be extended to Random Forest or others)
- **Features Used**: Scaled features from the dataset
- **Output**: Each record is predicted as 'Normal' or 'Congested'.
- **Metrics**: Confusion matrix, classification report

---

## 🖥️ Usage Instructions

1. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
2. **Run the app**:
   ```bash
   streamlit run app.py
   ```
3. **Open in browser**: Follow the Streamlit link (usually http://localhost:8501)
4. **Upload your CSV** and use the sidebar to:
   - Run Anomaly Detection
   - Predict Network Congestion

---

## 📈 Example Visualizations

- **Anomaly Distribution**: Histogram and pie chart of normal vs. anomalous records
- **Scatter Plot**: Anomalies over time
- **Congestion Distribution**: Pie chart of normal vs. congested records

---

## 📒 Project Structure

- `app.py` — Main Streamlit application
- `network-anomaly-and-congestion-prediction-model (1).ipynb` — Jupyter notebook with exploratory analysis and model development
- `requirements.txt` — Python dependencies
- `README.md` — Project documentation

---

## 📚 References & Credits

- [scikit-learn documentation](https://scikit-learn.org/)
- [Streamlit documentation](https://docs.streamlit.io/)
- [Plotly documentation](https://plotly.com/python/)
- Dataset: Example network traffic dataset (user-provided)

---

## 🙋‍♂️ Author & Contact

- Developed as a beginner project in network machine learning.
- For questions or suggestions, please open an issue or contact the project maintainer.
