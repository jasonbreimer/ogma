Will the Customer Accept the Coupon?

1.	Commands to start data investigation. This includes head(), sample(), and info(). I notice many columns have “object” or string types.
2.	Look into data with isnull(). The columns car, Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, and Restraunt20to50 contain null values. The column ‘car’ is entirely empty. Several entries (rows) are missing many attributes (columns).
A.	I should not use the “car” column
B.	I should filter out data with missing columns like: data.dropna(thresh=len(data.columns) - 5)
C.	When working with columns with missing data drop rows with incomplete data like: data.dropna(subset=['Bar', 'CoffeeHouse', 'CarryAway', 'RestaurantLessThan20','Restaurant20To50'])
3.	When looking at proportion of the total observations chose to accept the coupon (filtering missing rows):
fig1.png


4.	Use a bar plot to visualize the coupon column.
fig2.png

5.	Histogram to visualize the temperature column.
fig3.png
6.	On a filtered data set 41.19% contains bar coupons using a filtered data set.
7.	Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more is very similar at 62.49 and 62.13. This suggests that going to a bar more frequently often doesn’t increase coupon acceptance. 
8.	What about the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to all others. Is there a difference? Yes, the acceptance rate is slightly higher at 62.30% suggested younger age might increase coupon acceptance. 
9.	The same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry. This filtered group is slightly more likely than general population.
fig4.png
 
10.	Compare the acceptance rates between those drivers who:
Go to bars more than once a month, had passengers that were not a kid, and were not widowed: 62.31%
Go to bars more than once a month and are under the age of 30: 62.81%
Go to cheap restaurants more than 4 times a month and income is less than 50K: 59.40%
Acceptance rate of total population: 56.84%

11.	Drivers that have no kids, lower income, that go to bars and restaurants have higher likelihood of accepting a coupon.

12.	Additional exploration

a.	Drivers that went to less expensive restaurants (Restaurant(<20)) more likely to accept a coupon. 
b.	Lower income below <50 also more likely to accept a coupon. 
c.	Filtering on both shows 71.34% acceptance.
