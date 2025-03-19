### Driving Decisions: A Data-Driven Approach to Used Car Inventory Management

**Jason Reimer**

#### Executive summary
This project examines the features of used cars that influence their prices, particularly the manufacturer and model. It aims to identify actionable insights for dealerships to optimize inventory decisions and maximize value.

#### Rationale
In the competitive used car industry, dealerships vary in their approach to inventory—some offer a diverse range, while others specialize in specific types. This study seeks to uncover relationships between car features and prices to better inform inventory strategies and enhance dealership value.

#### Research Question
Which car manufacturer or model should used car dealerships focus on to maximize value?

### Project Findings Highlights

**Feature Engineering Impact:** Our analysis revealed two critical engineered features that significantly improved model performance:
- **Model Age Factor:** Car age impacts price differently by manufacturer, with the model_age_factor capturing how a vehicle's relative age within its model group affects valuation.
- **Premium Interaction:** The model_premium_interaction term effectively captures how premium status and model combine to influence pricing, providing more nuanced predictions.

**Model Performance:** After systematic evaluation of multiple algorithms, Random Forest emerged as the superior model with a test R² of 0.91 and MSE of 0.09, outperforming neural networks and traditional regression approaches.

**Price Stability Insights:** Analysis of manufacturer price volatility identified Ford Motor Company and Toyota Motor Corporation as having moderate and balanced price stability, with stability scores near 0.20 and positioned near the center of the distribution curve.

**Recommendations:** Dealerships should prioritize partnerships with large manufacturers like Ford and Toyota that offer broad model ranges while maintaining stable pricing. This strategic focus enables sourcing diverse inventory with predictable costs, making inventory management more reliable and efficient.

### Project Narrative Summary

#### Used Car Market Analysis: Manufacturer Impact and Price Stability

The goal of this project was to analyze the relationship between vehicle manufacturers, models, and price stability in the used car market. Through extensive data cleaning and preparation, we addressed numerous challenges including filtering out invalid entries, handling outliers, and implementing imputation techniques where appropriate. Our analysis revealed that different manufacturers have varying levels of influence on vehicle pricing, which led us to create interactive features that better capture these complex relationships. Starting with a Ridge regression model as our baseline, we evaluated several modeling approaches before settling on Random Forest as our best-performing solution, enhanced by our engineered features that reflect the subtle interplay between vehicle characteristics and price.

Our model revealed compelling insights about how vehicle age impacts price differently across manufacturers. By creating a `model_age_factor` feature, we captured how the relative age of each car within its model group affects its value retention. Similarly, we discovered that manufacturers with higher perceived "premium" status influence pricing in distinctive ways. The `model_premium_interaction` term we developed effectively captures this relationship, allowing for more nuanced price predictions that account for both model type and premium positioning. These findings highlight the importance of considering manufacturer-specific characteristics when evaluating used vehicles, rather than applying uniform depreciation assumptions across all makes and models.

Taking our analysis further, we examined price stability across manufacturers to identify those offering the most predictable and moderate pricing patterns. By plotting manufacturers along a Gaussian distribution based on their price volatility, we identified **Ford Motor Company** and **Toyota Motor Corporation** as standout examples of large manufacturers with diverse vehicle fleets and moderate price stability. Both companies demonstrated transformed stability scores near the center of the distribution (0.196 and 0.195 respectively), making them particularly valuable partners for dealerships seeking predictable inventory costs. Their extensive data points (29,591 for Ford and 19,249 for Toyota) across various models and price ranges further strengthens the reliability of these findings.

For dealerships in the National Used Car Association, these results offer clear strategic direction. We recommend prioritizing partnerships with larger manufacturers that offer a broad spectrum of models across various price ranges, with a particular focus on those maintaining more stable pricing patterns. By adopting this approach, dealerships can source diverse inventory with more predictable costs, mitigating price volatility and making inventory management more reliable and efficient. The Random Forest model we developed, with its impressive 0.91 R² score on test data, provides a robust foundation for pricing strategy. By leveraging the manufacturer-specific insights from our model, dealerships can make more informed decisions about which vehicles to acquire, when to adjust pricing, and how to optimize their inventory mix for both customer appeal and financial stability.

#### Outline of project

- [Link to Final Capstone Jupyter](https://github.com/jasonbreimer/ogma/blob/main/capstone_final/capstone_final.ipynb)


##### Contact and Further Information
email: rud90j@gmail.com

