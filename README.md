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

There are a couple of positive takeaways. There is only one high p-value. We see a pretty high R^2 (.701), and

The skew coefficient (0.7) is acceptable, too.

The RMSE is 121054

![Screen Shot 2020-11-28 at 1 08 15 PM](https://user-images.githubusercontent.com/72099238/100524096-cb35bd80-317a-11eb-81b0-8e0d59608ec8.png)

The residual does not fit perfectly on the line. The outliers in the tail that tell us ...

It is right-skewed (or positively skewed). May need to log transform to solve it.

# Second Model


![Screen Shot 2020-11-28 at 1 16 57 PM](https://user-images.githubusercontent.com/72099238/100524259-392eb480-317c-11eb-8363-4d91bf032ae1.png)


![Screen Shot 2020-11-28 at 1 17 07 PM](https://user-images.githubusercontent.com/72099238/100524233-0a184300-317c-11eb-8777-48fe105ecabe.png)

There were quite a few key takeaways from our model. Perhaps the most important one is that location matters. Homes with a waterfront and a high view rating tend to be more valuable. We are also able to make conclusions about the latitudes and longitudes of homes. After separating the county into north/central/south as well as west/central/east regions, we could see that the neighborhoods in the north and west regions tend to fare better than homes in the other regions. The inclusion of the regional information greatly reduced the error in our model.

The importance of condition is also an important takeaway, as homes with the highest condition rating were valued much higher than homes from the rest of the sample. This is a point of emphasis because condition can be controlled by homeowners. Another takeaway is that older homes in our sample had more value. While the year of construction did not make a massive difference, it was statistically significant and therefore worth including in our model.

If we had more resources to take this project further, there are a few topics we would like to investigate. One of those is the relevance of school districts and how much more valuable homes that are in premier school districts are. Another variable that could be relevant to our research is the age groups of homebuyers.
Certain features may be more important among different ages of homebuyers. Some features may not appear significant but could be if we can dive deeper.
We would also like to dive deeper into the grade variable. While it is clear that higher grades lead to higher value, based on the information given, it is difficult to determine the factors that determine grade. We are interested in what steps homeowners can take, if any, to improve the grade of their home. The more control homeowners have over this, the more emphasis we would like to place on this.
