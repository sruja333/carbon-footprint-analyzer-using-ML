# 🌍 Carbon Footprint Tracker

An interactive web app that helps users estimate their monthly carbon footprint based on lifestyle habits — including travel, home energy use, diet, waste, and shopping behavior.

Built with ❤️ using **FastAPI**, **React**, and **Machine Learning**.

---

## 🚀 Features

### 🧭 Categories
The app collects user data across key lifestyle areas:

| Category | Example Inputs |
|-----------|----------------|
| 🚗 **Travel & Transport** | Daily travel distance, transport mode, carpooling habits |
| 🏠 **Home Energy** | Electricity usage, AC usage, renewable energy sources |
| 🍔 **Food & Diet** | Meat & dairy consumption, local food preference |
| ♻️ **Waste & Water** | Waste generation, recycling habits, water usage |
| 🛍️ **Lifestyle Extras** | Shopping frequency, online orders |

---

## 🧮 How It Works

1. **Frontend (React / Lovable)**  
   - Collects user inputs via sliders and dropdowns.  
   - Sends the data to the FastAPI backend through an API request.

2. **Backend (FastAPI)**  
   - Loads a trained ML model (`footprint_model.pkl`).
   - Encodes categorical inputs.
   - Predicts an estimated **carbon footprint (kg CO₂/month)**.
   - Returns the result as JSON.

3. **Machine Learning Model**
   - A regression model trained on environmental behavior data (custom or Kaggle-based).
   - Uses emission factors to estimate total footprint.

