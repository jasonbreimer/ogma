Will the Customer Accept the Coupon?
- Commands to start data investigation: This includes head(), sample(), and info(). I notice many columns have “object” or string types.
- Look into data with isnull(): The columns car, Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, and Restaurant20to50 contain null values. The column car is entirely empty. Several entries (rows) are missing many attributes (columns).
    - A:  I should not use the car column.
    - B:  I should filter out data with missing columns like: data.dropna(thresh=len(data.columns) - 5).
    - C:  When working with columns with missing data, drop rows with incomplete data like: data.dropna(subset=['Bar', 'CoffeeHouse', 'CarryAway', 'RestaurantLessThan20', 'Restaurant20To50']).
- When looking at the proportion of the total observations that chose to accept the coupon (filtering missing rows):
**Figure 1**
- Use a bar plot to visualize the coupon column:
**Figure 2**
- Histogram to visualize the temperature column:
**Figure 3**
- On a filtered data set, 41.19% contains bar coupons.
- Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more. The rates are very similar at 62.49% and 62.13%. This suggests that going to a bar more frequently doesn’t significantly increase coupon acceptance.
- What about the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 compared to all others? Yes, the acceptance rate is slightly higher at 62.30%, suggesting younger age might increase coupon acceptance.
- The same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not kids and had occupations other than farming, fishing, or forestry. This filtered group is slightly more likely than the general population.
**Figure 4**
- Compare the acceptance rates between those drivers who:
    - Go to bars more than once a month, had passengers that were not kids, and were not widowed: 62.31%
    - Go to bars more than once a month and are under the age of 30: 62.81%
    - Go to cheap restaurants more than 4 times a month and income is less than 50K: 59.40%
    - Acceptance rate of the total population: 56.84%
- Drivers that have no kids, lower income, and go to bars and restaurants have a higher likelihood of accepting a coupon.
- Additional exploration:
    - Drivers that went to less expensive restaurants (Restaurant(<20)) are more likely to accept a coupon.
    - Lower income below 50K is also more likely to accept a coupon.
    - Filtering on both shows a 71.34% acceptance rate.
This should make your markdown more readable and structured. Let me know if you need any further adjustments or have more questions!
