### Driving Decisions: A Data-Driven Approach to Used Car Inventory Management

**Jason Reimer**

#### Executive summary
This project examines the features of used cars that influence their prices, aiming to identify actionable insights for dealerships to optimize inventory decisions and maximize value.

#### Rationale
In the competitive used car industry, dealerships vary in their approach to inventory—some offer a diverse range, while others specialize in specific types. This study seeks to uncover relationships between car features and prices to better inform inventory strategies and enhance dealership value.

#### Research Question
Which car manufacturer or model should used car dealerships focus on to maximize value?

#### Data Sources
The source is a dataset (vehicles.csv) containing information on 426K used cars.

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
Premium Value Influence: Manufacturers with a higher perceived "premium" value influence prices differently. This led to the creation of a new feature, c_premium, mapping a premium value score to manufacturers. This feature, combined with the model information, produced the model_premium_interaction term.

Car Age Influence: The influence of car age on price varies by manufacturer, resulting in the creation of the model_age_factor. This feature was used to develop the model/car age interaction term.

Model Explanation:
The model_age_factor reflects the relative age of each car within its model group. If a car's log_car_age is above the average for its model, its model_age_factor will be greater than 1, and if below average, less than 1.
The model_premium_interaction captures the combined effects of the car model and its premium status on the target variable, providing a more nuanced prediction.

#### Next steps
Price Trend Analysis: Analyze price trends by manufacturer to identify those with the most stable prices over time.

#### Outline of project

- [Link to notebook 1]()
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information
email: rud90j@gmail.com
