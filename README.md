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

There were quite a few key takeaways from our model. Perhaps the most important one is that location matters. Homes with a waterfront and a high view rating tend to be more valuable. We are also able to make conclusions about the latitudes and longitudes of homes. After separating the county into north/central/south as well as west/central/east regions, we could see that the neighborhoods in the north and west regions tend to fare better than homes in the other regions. The inclusion of the regional information greatly reduced the error in our model.

The importance of condition is also an important takeaway, as homes with the highest condition rating were valued much higher than homes from the rest of the sample. This is a point of emphasis because condition can be controlled by homeowners. Another takeaway is that older homes in our sample had more value. While the year of construction did not make a massive difference, it was statistically significant and therefore worth including in our model.

If we had more resources to take this project further, there are a few topics we would like to investigate. One of those is the relevance of school districts and how much more valuable homes that are in premier school districts are. Another variable that could be relevant to our research is the age groups of homebuyers.
Certain features may be more important among different ages of homebuyers. Some features may not appear significant but could be if we can dive deeper.
We would also like to dive deeper into the grade variable. While it is clear that higher grades lead to higher value, based on the information given, it is difficult to determine the factors that determine grade. We are interested in what steps homeowners can take, if any, to improve the grade of their home. The more control homeowners have over this, the more emphasis we would like to place on this.
