# california-housing-prices
An end-to-end project from Hands-On ML by O'Reilly (1st project of the book)
The project imitates a work setting project. The problem is framed as a roleplay.

# The problem
Your boss answers that your model’s output (a prediction of a district’s median housing price) will be fed to another Machine Learning system, along with many other signals. This downstream system will determine whether it is worth investing in a given area or not. Getting this right is critical, as it directly affects revenue.

# What does the current solution look like?
Your boss answers that the district housing prices are currently estimated manually
by experts: a team gathers up-to-date information about a district, and when they
cannot get the median housing price, they estimate it using complex rules.
This is costly and time-consuming, and their estimates are not great; in cases where
they manage to find out the actual median housing price, they often realize that their
estimates were off by more than 20%. This is why the company thinks that it would
be useful to train a model to predict a district’s median housing price given other data
about that district. The census data looks like a great dataset to exploit for this pur‐
pose, since it includes the median housing prices of thousands of districts, as well as
other data.

# Type of ML task
This is a supervised multiple univariate regression task. Plain batch learning should be fine as there is no continuous flow of data, no particular need to adjust to changing data rapidly, and the data is small enough to fit into memory.

# Select a performance measure
Typically for regression problems you use the Root Mean Square Error (RMSE). 

# The assumptions
The model needs to output estimated prices of houses in dollars.

# Dataset
The median house income is represented in roughly tens of thousands of dollars
Median age and median house value has been capped. The cap on the value might be a serious issue since it is the variable that will be predicted.