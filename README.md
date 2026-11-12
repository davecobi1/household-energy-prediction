# Household Energy Consumption Prediction

A machine learning project exploring the prediction of monthly household energy consumption using a feedforward neural network.

The notebook walks through data exploration, feature selection, train/test splitting, feature scaling, model training, and a comparison between a neural network regressor and Scikit-learn's Linear Regression.

## Project overview

The goal is to predict **monthly household energy consumption (kWh)** from the household-related input features in the dataset.

Models used:
- **Neural network regressor:** a small feedforward network with two ReLU hidden layers and a linear output layer.
- **Linear Regression:** a Scikit-learn baseline used for comparison.

This is a learning project. The notebook is intended to document the modelling process and provide an opportunity to compare two regression approaches.

## Repository structure

```text
household-energy-prediction/
├── data/
│   └── household_energy_consumption_1800.csv
├── ml_testbed.ipynb
├── README.md
└── requirements.txt
```

## Getting started

1. Clone or download this repository.
2. Make sure the dataset CSV is inside the `data/` folder.
3. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open `ml_testbed.ipynb` and run the cells.

The notebook should load the dataset using a relative path such as:

```python
data = "data/household_energy_consumption_1800.csv"
df = pd.read_csv(data)
```

## Workflow

The notebook covers:

1. Importing the required libraries and loading the dataset.
2. Inspecting the dataset and checking for missing values and duplicates.
3. Exploring distributions, correlations, and selected feature relationships.
4. Separating the input features from the target (`monthly_energy_consumption_kwh`).
5. Splitting the data into training and test sets.
6. Scaling the input features with `MinMaxScaler`.
7. Building and training a feedforward neural network for regression.
8. Training a Scikit-learn Linear Regression baseline.
9. Comparing model predictions with visualisations.

## Evaluation

The notebook uses a held-out test set to compare predictions from the two models. Review the evaluation cells and their printed metrics after running the notebook.

Results can vary if the dataset, preprocessing, model settings, or random split are changed. No performance claim is made here without the corresponding test-set results.

## Dataset and attribution

The dataset used in this project is attributed to:

- **Creators:** Georges Hebrail and Alice Berard
- **UCI Machine Learning Repository DOI:** [10.24432/C58K54](https://doi.org/10.24432/C58K54)
- **License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

The CC BY 4.0 license permits sharing and adaptation with appropriate attribution. If the CSV in this repository is a cleaned, sampled, or otherwise modified version of the original UCI data, those changes should be clearly identified.

## Notes

- This project is for learning and experimentation, not for operational energy billing or engineering decisions.
- The neural network is a **regression model** because it predicts a continuous numerical value.
- The final output layer uses a linear activation; the ReLU hidden layers allow the network to learn nonlinear relationships.

## Author

Created as part of my ongoing learning in machine learning and its applications to energy-related problems.
