# King County Home Value Analysis
Our goal is provide insight to real estate agencies that help people in the housing market. Specifically, we are seeking to determine factors that make a significant impact on price. To draw these conclusions, we used data from about 21,000 King County homes and their characteristics such as bathrooms/Bedrooms, square feet, condition, grade, floors, location (latitude/longitude/waterfront), and year built.

# Applications Used:
* Jupyter notebook
* Pandas
* Matplotlib
* Numpy
* Sklearn
* Statsmodels

# Base Model
![Screen Shot 2020-11-28 at 1 05 40 PM](https://user-images.githubusercontent.com/72099238/100524052-7b56f680-317a-11eb-87e8-065c8d4d7f54.png)

There are a couple of positive takeaways. There is only one high p-value. We see a pretty high R^2 (.701).

The skew coefficient (0.7) is acceptable, as well.

The RMSE is 121,054.

![Screen Shot 2020-11-28 at 1 08 15 PM](https://user-images.githubusercontent.com/72099238/100524096-cb35bd80-317a-11eb-81b0-8e0d59608ec8.png)

* The residual does not fit perfectly on the line. The outliers in the tail that tell us it is right-skewed (or positively skewed). May need to log transform to solve this issue.

# Second Model

On this model, we focus on categorical variables and made it dummies

![Screen Shot 2020-11-28 at 1 20 25 PM](https://user-images.githubusercontent.com/72099238/100524298-86ab2180-317c-11eb-988d-4358ba462383.png)


![Screen Shot 2020-11-28 at 1 20 39 PM](https://user-images.githubusercontent.com/72099238/100524302-90348980-317c-11eb-90ba-dd18880a1b62.png)


* R_squared is .602 that lower than basemodel and RMSE is 140227 that higher than basemodel. 

* This model is definitely worse than base model

# Third Model

On this model, we decided to bin bedrooms, bathrooms, lat, long and zipcode

![Screen Shot 2020-11-28 at 1 27 43 PM](https://user-images.githubusercontent.com/72099238/100524412-9c6d1680-317d-11eb-8969-8098910bfd52.png)

![Screen Shot 2020-11-28 at 1 27 55 PM](https://user-images.githubusercontent.com/72099238/100524417-a42cbb00-317d-11eb-9a6a-b5cd6ce2f085.png)

![Screen Shot 2020-11-28 at 1 30 06 PM](https://user-images.githubusercontent.com/72099238/100524439-da6a3a80-317d-11eb-88f0-736fbfdb8899.png)


* The residual does not fit perfectly on the line. The outliers in the tail that tell us It is a right skewed (or positive skewed). May need to log transform to solve it.

* Compare the third model to the base model. The R2 and RMSE are almost the same, but on the third model, I already solved all problems, such as: multicollinearity, high correlation and dummy variable.

* Based on our experience, the third model is the best model thus far. We attempted to use log transformations, but that made our model less effective. However, we will try again with log transformation, and we will see if it can help our model become more normalized.

# Forth Model

On this model, we will log transformation to help our model become more normalized.

![Screen Shot 2020-11-28 at 1 33 15 PM](https://user-images.githubusercontent.com/72099238/100524518-6e3c0680-317e-11eb-83e7-ded78f3171ed.png)

There are some independent variables that we need to log transformation

![Screen Shot 2020-11-28 at 1 35 45 PM](https://user-images.githubusercontent.com/72099238/100524540-a7747680-317e-11eb-8ece-c80991dc9e80.png)

![Screen Shot 2020-11-28 at 1 35 55 PM](https://user-images.githubusercontent.com/72099238/100524544-a93e3a00-317e-11eb-874d-37ce26f82e5c.png)

![Screen Shot 2020-11-28 at 1 36 32 PM](https://user-images.githubusercontent.com/72099238/100524550-be1acd80-317e-11eb-9a8f-872c7e64139a.png)

* R^2 is improved, but this model with log dependent and is complicated to interpret. In addition, the qq plot is now left skewed. 

* So, we decided to take the third model as our final choice. It has a 0.697 R-squared and RMSE just over 120,000.

* Fortunately, there is a significant reduction in RMSE since that initial model.

# Conclusion
* There were quite a few key takeaways from our model. Perhaps the most important one is that location matters. Homes with a waterfront and a high view rating tend to be more valuable. We are also able to make conclusions about the latitudes and longitudes of homes. After separating the county into north/central/south as well as west/central/east regions, we could see that the neighborhoods in the north and west regions tend to fare better than homes in the other regions. The inclusion of the regional information greatly reduced the error in our model.

* The importance of condition is also an important takeaway, as homes with the highest condition rating were valued much higher than homes from the rest of the sample. This is a point of emphasis because condition can be controlled by homeowners. Another takeaway is that older homes in our sample had more value. While the year of construction did not make a massive difference, it was statistically significant and therefore worth including in our model.

* If we had more resources to take this project further, there are a few topics we would like to investigate. One of those is the relevance of school districts and how much more valuable homes that are in premier school districts are. Another variable that could be relevant to our research is the age groups of homebuyers.
Certain features may be more important among different ages of homebuyers. Some features may not appear significant but could be if we can dive deeper.
We would also like to dive deeper into the grade variable. While it is clear that higher grades lead to higher value, based on the information given, it is difficult to determine the factors that determine grade. We are interested in what steps homeowners can take, if any, to improve the grade of their home. The more control homeowners have over this, the more emphasis we would like to place on this.
