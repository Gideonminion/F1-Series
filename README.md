# 🏎️ F1 Race Time Prediction using Machine Learning

This project demonstrates how to use machine learning to predict F1 race times based on qualifying performance and historical race data, leveraging the [`FastF1`] library.

---

## 📌 Project Goal

The objective is to predict the potential race times for drivers in the **2025 Grand Prix** using:

- Hypothetical qualifying times for 2025  
- Historical lap and sector times from the **2024 Grand Prix**

---

## ⚙️ Setup

To run this project, make sure you have the following Python libraries installed:

- `fastf1`
- `pandas`
- `numpy`
- `scikit-learn`

You can install them via pip:

```bash
pip install fastf1 pandas numpy scikit-learn


General Breakdown
1. Installation and Imports
Installs and imports required packages like fastf1, pandas, numpy, and scikit-learn.

2. Cache Setup
Configures a local cache directory for fastf1 to optimize data loading.

3. Data Loading
Loads race data from the 2024 Australian Grand Prix using fastf1.

4. Data Preparation
Extracts and cleans lap time data.

Converts lap times into seconds for easier processing.

5. Hypothetical Qualifying Data
Creates a fictional dataset for 2025 Chinese Grand Prix qualifying times for selected drivers.

6. Driver Mapping
Maps full driver names to their three-letter driver codes (e.g., VER, HAM) to align datasets.

7. Data Merging
Merges 2025 qualifying data with 2024 historical lap times using driver codes as keys.

8. Model Training
Splits the data into training and testing sets.

Trains a Gradient Boosting Regressor to predict race lap times based on qualifying performance.

9. Prediction
Uses the trained model to predict race lap times for the hypothetical 2025 Chinese Grand Prix.

10. Results and Evaluation
Displays predicted race times sorted by performance.

Evaluates the model using Mean Absolute Error (MAE) on the test set.

📊 Output Example
The final output includes:

A ranked table of drivers by predicted race times.

The MAE indicating prediction accuracy.

Prediction + Sector Timing
Next Work: Incorporate pitstop timing, weather data for more granular predictions.
