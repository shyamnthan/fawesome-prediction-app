# fawesome-prediction-app
This project contains SARIMAX models to forecast average watch time (AWT) for three AVOD channels on the Fawesome platform. A web app built with Streamlit allows users to input key variables and generate real-time predictions for channel-specific AWT.
# Fawesome AWT Prediction App

This project hosts three pre-trained SARIMAX models to predict **Average Watch Time (AWT)** for three AVOD channels on the Fawesome platform: `faw_com`, `faw_fir`, and `faw_rok`.

Each model uses rolling SARIMAX predictions based on key user metrics such as:
- Total Unique Users
- Ad Fill Rate (FR)
- Unique Users by Source (e.g., search, store, homepage)

## 📁 Project Structure

```
final/
│
├── faw_com/
│   ├── sarimax_model_all_vars.pkl
│   ├── cleaned_data.csv
│   └── ...
│
├── faw_fir/
│   ├── sarimax_model_all_vars.pkl
│   ├── cleaned_data.csv
│   └── ...
│
├── faw_rok/
│   ├── sarimax_model_all_vars.pkl
│   ├── cleaned_data.csv
│   └── ...
```

## 🚀 How to Use

A Streamlit web app will allow you to:
- Select a channel
- Input predictor variables
- Get a prediction for AWT

### 🧠 Models
Each model is saved as a `.pkl` file and can be loaded using Python's `pickle` module.

## 🔧 Setup

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the app:
   ```bash
   streamlit run app/app.py
   ```

## 🛠 Dependencies

See [`requirements.txt`](./requirements.txt)

## 📊 Output
Each channel directory contains:
- Raw and cleaned data
- Input and prediction files (`.xlsx`)
- Trained SARIMAX model (`.pkl`)
