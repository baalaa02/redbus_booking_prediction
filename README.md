# redbus_booking_prediction
 # 🚌 redBus Data Decode 2025 – Final Submission

This repository contains my solution for the **redBus Data Decode 2025** hackathon hosted on Analytics Vidhya. The objective was to build a predictive model that forecasts the final number of booked seats for a given route **15 days before the journey date**.

---

## 📌 Problem Statement

Given historical transactional and search data for bus routes, predict the **final seat count** per route for future journeys. This helps redBus optimize inventory and improve operational decisions in advance.

---

## 💡 Approach

- **Data Preparation & Cleaning**:
  - Merged transaction and search data on `doj`, `srcid`, and `destid`.
  - Filled missing values and dropped unused columns.
  - Extracted useful date features like journey day, month, and weekday from the `doj` field.

- **Feature Engineering**:
  - Calculated cumulative seat counts and search counts.
  - Encoded categorical variables like regions and tiers using `LabelEncoder`.

- **Model Building**:
  - Used `RandomForestRegressor` from `scikit-learn` for training.
  - Evaluated the model using RMSE to ensure reliable performance.

- **Prediction**:
  - Predictions were generated for the test data.
  - All predicted seat counts were rounded to the nearest whole number, as partial seats do not make sense in real-world scenarios.

- **Final Output**:
  - Created `submission.csv` with the required structure: `route_key`, `final_seatcount`.

---

## 📁 Files

- `redbus_solution.ipynb` – Full notebook from data processing to final model.
- `submission.csv` – Final submission file.
- `sample_submission.csv` – Provided template used for format reference.

---

## 🚀 How to Run

1. Clone this repo and open the notebook in Jupyter/Colab.
2. Place the datasets (`train.csv`, `test.csv`, `transactions.csv`, `search_data.csv`, etc.) in the working directory.
3. Run the notebook cells sequentially.
4. The final predictions will be saved as `submission.csv`.

---

## 🙌 Acknowledgements

Special thanks to Analytics Vidhya and redBus for organizing this challenge. This project helped me deepen my understanding of time-based feature engineering, merging datasets, and deploying regression models in real-world-like scenarios.

---

