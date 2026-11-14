# NASA C-MAPSS Remaining Useful Life (RUL) Prediction

## Project Overview

This project focuses on predictive maintenance of aircraft engines using Machine Learning regression techniques.

It uses NASA's C-MAPSS Turbofan Engine Degradation Simulation Dataset (FD001) to estimate the Remaining Useful Life (RUL) of aircraft engines based on operational and sensor data.

The objective is to compare different regression models and identify an effective approach for predicting engine degradation.

## Objectives

- Analyse aircraft engine sensor data.
- Perform exploratory data analysis and preprocessing.
- Calculate Remaining Useful Life (RUL).
- Train and compare three regression models.
- Evaluate model performance using standard regression metrics.
- Save and reuse the best-performing trained model.

## Dataset

**Dataset:** NASA C-MAPSS FD001

The dataset contains operational settings and sensor measurements collected from simulated aircraft engine run-to-failure trajectories.

Dataset source: [NASA Prognostics Data Repository](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/)

The raw dataset is not included in this repository. Download it separately and place the required FD001 files in the data directory configured in the notebook.

## Machine Learning Models

Three regression algorithms were implemented:

1. Linear Regression
2. Random Forest Regressor
3. Gradient Boosting Regressor

Gradient Boosting was selected as the final model based on validation performance.

## Model Performance

### Final Test Results

| Metric | Capped RUL | Original Uncapped RUL |
|---|---:|---:|
| MAE | 11.9845 | 13.0545 |
| MSE | 288.3114 | 331.5180 |
| RMSE | 16.9797 | 18.2076 |
| R² Score | 0.8205 | 0.8080 |

The training target uses a maximum RUL threshold of 125 cycles. Both capped and original uncapped test evaluations are reported.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Project Structure

```text
NASA-CMAPSS-RUL-Prediction/
│
├── data/
│   └── Dataset files (download separately)
│
├── models/
│   └── best_rul_model.pkl
│
├── notebooks/
│   └── NASA_CMAPSS_RUL_Prediction.ipynb
│
├── results/
│   ├── feature_importance.csv
│   ├── final_test_results.csv
│   ├── test_predictions.csv
│   ├── uncapped_test_results.csv
│   └── validation_results.csv
│
├── .gitignore
├── README.md
└── requirements.txt
```

## How to Run the Project

1. Clone the repository.
2. Download and extract the NASA C-MAPSS FD001 dataset.
3. Place the required dataset files in the appropriate data directory.
4. Install the required Python dependencies.
5. Open the Jupyter Notebook in VS Code or Jupyter.
6. Execute the notebook cells sequentially.

## Future Scope

- Experiment with advanced regression algorithms.
- Explore deep learning approaches such as LSTM.
- Improve RUL prediction accuracy.
- Develop an interactive predictive maintenance dashboard.
- Extend the approach to additional NASA C-MAPSS subsets.

## Project Outcome

The project demonstrates how machine learning regression techniques can support predictive maintenance by estimating the remaining useful life of aircraft engines and helping identify potential maintenance requirements before failure.

---

**Project Domain:** Machine Learning | Predictive Maintenance | Regression

**Dataset:** NASA C-MAPSS FD001
