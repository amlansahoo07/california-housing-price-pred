# California Housing Price Predictor

## Project Overview
This project aims to build a predictive model for estimating the median housing price in California based on census data. The dataset includes various socio-economic and geographical features that influence housing prices, such as median income, population, and location.

## Dataset
The project utilizes the California housing dataset, which contains the following key attributes:
- `longitude`, `latitude`: Geographical coordinates
- `housing_median_age`: Age of the housing unit
- `total_rooms`, `total_bedrooms`: Number of rooms and bedrooms per district
- `population`, `households`: Population size and number of households
- `median_income`: Median income of residents
- `ocean_proximity`: Categorical feature indicating proximity to the ocean
- `median_house_value`: Target variable representing median house price

## Project Pipeline
<img width="883" alt="image" src="https://github.com/user-attachments/assets/01aa183c-5a1c-4449-97c9-902617ac6217" />

The project follows a structured ML workflow:
1. **Data Acquisition**: Downloading and loading the dataset from a remote source.
2. **Exploratory Data Analysis (EDA)**: Understanding data distribution through histograms, scatter plots, and correlation analysis.

   <img width="360" alt="image" src="https://github.com/user-attachments/assets/91cfb1b4-52bf-4660-be25-e65ac26d67c7" /> <img width="256" alt="image" src="https://github.com/user-attachments/assets/63f48da1-6780-4693-a8a0-cc7877c93225" />
4. **Data Preprocessing**:
   - Handling missing values using median imputation.
   - Encoding categorical variables using One-Hot Encoding.
   - Feature engineering (e.g., creating new ratio-based features).
   - Feature scaling using Standardization.
5. **Model Training and Evaluation**:
   - Leveraging Scikit-learn's `Pipeline` and `ColumnTransformer` to streamline preprocessing and modeling.
   - Training multiple models, including Linear Regression, Decision Trees, and Random Forest.
   - Using Cross-Validation for performance assessment.
   - Hyperparameter tuning using Grid Search and Randomized Search.
6. **Final Model Selection**:
   - Selecting the best-performing model based on evaluation metrics.
   - Analyzing feature importance for interpretability.
7. **Testing and Deployment**:
   - Evaluating the model on a separate test set.
   - Computing confidence intervals for performance robustness.

## Results
- The final model was a tuned **Random Forest Regressor**.
- Reduced RMSE from **~68,000 USD** (Linear Regression) to **~41,000 USD** (Tuned Random Forest), significantly improving prediction accuracy for house prices ranging from 120,000 to 500,000 USD.
- Feature importance analysis showed that `median_income` had the strongest influence on house prices.

## License
This project is licensed under the [MIT LICENSE](LICENSE).
