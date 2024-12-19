# ML Lab Evaluation
This work is submitted for the lab evaluation of the course Machine learning (UML501). This project aims to predict the performance of a fuel cell using machine learning techniques. 

## Methodology

1. **Data Loading and Preprocessing:**
   - The dataset is loaded using Pandas.
   - Columns ('Target1', 'Target2', 'Target3', 'Target4') are dropped according to instructions.
   - PyCaret's `setup` function is used for preprocessing, including:
     - Data splitting (70% train, 30% test)
     - Normalization (Robust scaler)
     - Transformation (Yeo-Johnson)
     - PCA (Incremental)
     - Outlier removal (5% threshold)

2. **Model Selection and Evaluation:**
   - PyCaret's `compare_models` function is used to compare various regression models.
   - The best-performing model is selected based on evaluation metrics (R-squared).
   - The `evaluate_model` function provides detailed insights into the selected model's performance.

3. **Prediction and Visualization:**
   - The `predict_model` function is used to make predictions on new data.
   - The `plot_model` function is used to visualize feature importance and prediction errors.

## Results

- The best-performing model is `Bayesian Ridge` with an R-squared value of `0.6854`.


