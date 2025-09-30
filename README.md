
# 🏠 House Price Prediction

This repository contains a machine learning project for predicting house prices using Python (Flask backend) and a JavaScript/TypeScript client (Next.js/Bun).


## ✨ Features
- 🚀 REST API for house price prediction
- 🤖 Supports multiple models (Linear Regression, Random Forest)
- 🛠️ Scalable feature engineering
- 🖥️ Frontend client for user interaction


## 📁 Project Structure
```
model.py
processing.py
utils.py
app.py
requirements.txt
LICENSE
client/
   src/
   public/
   ...
dataset/
   clean_house_dataset.csv
   house_dataset.csv
models/
   house_price_scaler.pkl
   house_train_columns.json
   lr_model.joblib
   rf_model.joblib
```


## 🚦 Getting Started

### 🐍 Backend
1. Create and activate a Python virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the server:
   ```bash
   python app.py
   ```

### 🌐 Frontend
1. Go to the client directory:
   ```bash
   cd client
   ```
2. Install dependencies:
   ```bash
   bun install
   ```
3. Run the client:
   ```bash
   bun dev
   ```


## 📡 API Usage
- `POST /predict?model=lr|rf`
   - JSON body:
      ```json
      {
         "Size_sqft": 1200,
         "Bedrooms": 3,
         "Bathrooms": 2,
         "YearBuilt": 2010,
         "Location": "City"
      }
      ```
   - Response:
      ```json
      {
         "model_used": "Linear regression",
         "input": { ... },
         "prediction": 123456.78
      }
      ```


## 📜 License
MIT
