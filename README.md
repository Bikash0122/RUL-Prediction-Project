# Predictive Maintenance: Turbofan Engine RUL Forecasting

A machine learning project to predict the Remaining Useful Life (RUL) of turbofan engines using the NASA CMAPSS dataset and a Random Forest Regressor.

---

## 📋 Table of Contents
* [Project Objective](#-project-objective)
* [Dataset](#-dataset)
* [Technical Methodology](#-technical-methodology)
* [Results & Key Achievements](#-results--key-achievements)
* [How to Run](#-how-to-run)
* [Tools & Technologies](#-tools--technologies)

---

## 🎯 Project Objective

To develop a robust machine learning model that accurately predicts the Remaining Useful Life (RUL) of critical turbofan engine components. The goal was to leverage time-series sensor data to forecast potential failures, enabling a strategic shift from traditional, time-based maintenance to a more efficient and cost-effective, condition-based maintenance schedule.

---

## 📊 Dataset

This project utilized the **NASA Turbofan Engine Degradation Simulation Dataset (CMAPSS - FD001)**. 

This is a benchmark time-series dataset containing simulated data from 100 engines. Each engine has 21 sensors monitoring performance and operational settings until the point of failure, making it ideal for developing predictive maintenance models.



---

## 🛠️ Technical Methodology

The project followed a structured machine learning workflow:

1.  **Data Preprocessing & Exploration**: Loaded the raw, unlabeled data and performed an Exploratory Data Analysis (EDA). This involved visualizing sensor trends over time to identify the most informative sensors that showed clear degradation patterns leading up to engine failure.

2.  **Feature Engineering**: Calculated the target variable, **RUL**, for the training dataset. To capture operational trends, new features were engineered by calculating rolling statistics (e.g., mean, standard deviation) for key sensor readings over a defined time window.

3.  **Model Selection & Rationale**: A **Random Forest Regressor** was selected for this task.
    * **Rationale**: This ensemble model is highly effective for complex regression problems on tabular data. It is robust to overfitting, can capture non-linear relationships, and provides valuable insights into feature importance without requiring extensive data scaling.

4.  **Training & Evaluation**: The dataset was split into a training set (80%) and a testing set (20%). The model was trained exclusively on the training data and its performance was rigorously evaluated on the unseen test data.

---

## ✨ Results & Key Achievements

The final model demonstrated strong predictive capabilities for forecasting engine failure.

* **Successfully engineered insightful time-series features** (e.g., rolling averages, standard deviations) to effectively capture engine degradation trends.
* Achieved a **Root Mean Squared Error (RMSE) of 15.88 cycles** on the test data (after clipping predictions, down from 19.8). This indicates the model's RUL predictions are, on average, off by approximately 16 cycles.
* The model explained **85% of the variance** in the data, as indicated by an **R-squared (R²) score of 0.85**.
* Validated a practical and effective methodology for predictive maintenance that is highly applicable to complex mechanical systems in aerospace and other industries.

---

## 🚀 How to Run

To run this project on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You may need to create a `requirements.txt` file containing pandas, numpy, scikit-learn, matplotlib, and seaborn).*

3.  **Run the notebook:**
    Open the `.ipynb` file in a Jupyter environment (like Jupyter Lab, VS Code, or Google Colab) and execute the cells.

---

## 💻 Tools & Technologies

* **Programming Language:** Python 🐍
* **Core Libraries:** Pandas, NumPy, Scikit-learn
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Google Colab (Jupyter Notebook)
