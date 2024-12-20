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

2. **Model Comparison and Selection:**
    - PyCaret's `compare_models` function is used to evaluate various regression models.
    - A list of 14 selected models is created for further analysis.
3. **Model Training and Evaluation:**
    - Each selected model is trained using PyCaret's `create_model` function.
    - Predictions are made on the entire dataset using `predict_model`.
    - PyCaret's `plot_model` function is used to visualize error, learning curves, and feature importance.
4. **Results and Metrics:**
    - Performance metrics (R2, MAE, MSE) are collected for each model using PyCaret's `pull` function.

## Results

The best-performing model is `Light Gradient Boosting Machine` with an R-squared value of `0.8589`. 
<br> <br>
**Scatter Plot**<br>
![image](https://github.com/user-attachments/assets/2ef5deba-93fd-4b9f-8267-dd37848ec464)
<br><br>
**Error plot** <br>
![image](https://github.com/user-attachments/assets/e14be9b9-fa98-4f16-8608-6a85d342e707)
<br><br>
**Learning Curve plot** <br>
![image](https://github.com/user-attachments/assets/3dc94af3-daa4-4678-bc4b-d51b8967ba7f)
<br><br>
**Feature selection plot** <br>
![image](https://github.com/user-attachments/assets/ae7d2aec-a6aa-4bc2-9931-f0dea218591c)

## Detailed Evaluation Metrics
  
|    | Model    |     R2 |     MAE |     MSE |
|---:|:---------|-------:|--------:|--------:|
| 1 | lightgbm | 0.8589 |  8.7586 | 278.159 |
| 2 | et       | 0.8537 |  7.312  | 288.352 |
| 3 | xgboost  | 0.849  |  7.1843 | 297.656 |
| 4 | gbr      | 0.8251 | 12.3605 | 344.759 |
| 5 | rf       | 0.8048 | 12.9297 | 384.815 |
| 6 | br       | 0.7257 | 17.6103 | 540.736 |
| 7 | ridge    | 0.7257 | 17.6282 | 540.812 |
| 8 | lr       | 0.7256 | 17.6507 | 540.962 |
| 9 | lar      | 0.7256 | 17.6507 | 540.962 |
| 10 | huber    | 0.7135 | 17.0503 | 564.773 |
| 11 | lasso    | 0.704  | 17.6874 | 583.525 |
| 12 | llar     | 0.704  | 17.6874 | 583.525 |
| 13 | par      | 0.6986 | 17.8317 | 594.096 |
| 14 | dt       | 0.6699 | 11.1087 | 650.635 |

