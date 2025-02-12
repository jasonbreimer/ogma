### Driving Decisions: A Data-Driven Approach to Used Car Inventory Management

**Jason Reimer**

#### Executive summary
This project examines the features of used cars that influence their prices, particularly the manufacturer and model. It aims to identify actionable insights for dealerships to optimize inventory decisions and maximize value.

#### Rationale
In the competitive used car industry, dealerships vary in their approach to inventory—some offer a diverse range, while others specialize in specific types. This study seeks to uncover relationships between car features and prices to better inform inventory strategies and enhance dealership value.

#### Research Question
Which car manufacturer or model should used car dealerships focus on to maximize value?

#### Data Sources
The source is a dataset (vehicles.csv) containing information on 426K used cars also included in the /data directory vehicles.zip.
The cleaned data file (capstone_ready.csv) has also been included and placed in the root directory called capston_ready.zip.

#### Methodology
1. Data Cleaning: Preprocess data to ensure accuracy.
2. Handling Missing Values: Drop or impute missing values based on MSE score changes.
3. Exploratory Data Analysis: Use LOWESS charting to understand feature distributions.
4. Initial Modeling: Build a basic model to establish a baseline.
5. Interaction Terms: Examine interactive terms between features.
6. Polynomial Adjustments: Adjust for polynomial relationships.
7. Feature Engineering: Create new features to enhance model performance.
8. Final Model: Develop a refined model using the newly created features.

#### Results

Findings:

Model Age Influence: The influence of car age on price varies by manufacturer. The model_age_factor reflects this variation, showing that the relative age of each car within its model group impacts its price.

Premium Influence: Manufacturers with a higher perceived "premium" value influence prices differently. The model_premium_interaction term captures the combined effects of the car model and its premium status on the price, providing a more nuanced prediction.

Recommendations:
Dealerships should prioritize partnering with large manufacturers due to the broad spectrum of models they offer across various price ranges. Additionally, focus on manufacturers that maintain more stable pricing, enabling dealerships to source a diverse range of models with predictable costs. This strategic focus mitigates price volatility, making inventory management more reliable and efficient.

#### Next steps
Price Trend Analysis: Analyze price trends by manufacturer to identify those with the most stable prices over time.

#### Outline of project

- [Link to notebook 1](https://github.com/jasonbreimer/ogma/blob/4ef0e2c8d4bdfc8e1152ebdd2972e126b9861ece/capstone/capstone_preview.ipynb)



##### Contact and Further Information
email: rud90j@gmail.com
