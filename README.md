# demo_ML_energy_buildings
# Energy Consumption and Greenhouse Gas Emissions Prediction for Seattle Buildings

## Project Description

This project aims to analyze and predict energy consumption and greenhouse gas (GHG) emissions of buildings in Seattle. The primary goals are to provide insights into energy usage patterns and to identify key factors influencing GHG emissions. The dataset comprises various features related to building characteristics and energy consumption metrics.

## Dataset

The dataset used in this project includes detailed information on buildings in Seattle, encompassing residential and non-residential types. Key features include building size, location (latitude and longitude), and energy usage statistics. Two main target variables were analyzed:

1. **Site Energy Use WN (Kbtu)**: Annual energy consumption of the property, adjusted for weather conditions.
2. **Total GHG Emissions**: Total greenhouse gas emissions in metric tons of CO2 equivalent.

## Exploratory Data Analysis (EDA)

1. **Missing Data Analysis**: Utilized `missingno` to visualize and address missing values.
2. **Distribution Analysis**: Pie charts and bar plots were used to show the distribution of building types and energy consumption by neighborhood.
3. **Correlation Analysis**: Scatter plots revealed a strong correlation between building size and energy consumption, with notable outliers such as medical and distribution centers.

## Feature Engineering

1. **Handling Missing Data**: Addressed missing values with appropriate imputation techniques.
2. **Outlier Detection**: Used Interquartile Range (IQR) method to identify and handle outliers.
3. **Categorical Encoding**: Applied One Hot Encoding and Label Encoding based on the model requirements.
4. **New Features Creation**: Created new variables to enhance model performance, including energy use per square meter and neighborhood-specific factors.

## Modeling Approach

1. **Model Selection**: Tested various regression models including Dummy Regressor, Random Forest Regressor, and Gradient Boosting Regressor.
2. **Hyperparameter Tuning**: Employed GridSearchCV for hyperparameter optimization.
3. **Model Evaluation**: Used cross-validation and performance metrics such as R2, RMSE, and MAE to evaluate models.

### Key Models and Findings:

- **Random Forest Regressor**:
  - Criterion: Quality measure of the split
  - Max Depth: Tree depth
  - Max Features: Number of features considered for the best split
  - N_estimators: Number of trees

- **Gradient Boosting Regressor**:
  - Learning Rate: Step size in gradient descent
  - Loss: Cost function used

Both ensemble models performed better than baseline models, with Random Forest showing slightly better generalization.

## Results

- **Performance Metrics**: Random Forest Regressor showed better performance with lower RMSE and higher R2 scores.
- **Error Analysis**: Predictions were generally underestimations, with larger errors in high consumption buildings. Log transformation of targets provided better error interpretation.
- **Variable Importance**: Total building area and type/use of buildings were significant predictors. Energy Star Score was a crucial feature in improving model accuracy.

## Conclusion

The project successfully demonstrated the importance of feature engineering and model tuning in predicting energy consumption and GHG emissions. Future work could focus on expanding the dataset and exploring additional modeling techniques to further improve predictive performance.

## How to Run

1. **Clone the repository**: `git clone <repo_url>`
2. **Install dependencies**: `pip install -r requirements.txt`
3. **Run the Jupyter notebook**: `jupyter notebook`
4. **Follow the steps in the notebook to load data, perform analysis, and run models`**

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- This project was completed as part of a data science training program.
- Special thanks to the instructors and peers for their valuable feedback and support.

## Author
Audrey Hohmann, OpenclassRoom student : Data Scientist training path
