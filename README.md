# ds-grads-spark-training
Links required to do Spark hands-on session;

**DataBricks**
https://community.cloud.databricks.com/

**PySpark cheatsheet**
https://www.datacamp.com/community/blog/pyspark-sql-cheat-sheet

**Titanic Dataset**
https://www.kaggle.com/c/titanic/data

**Wine Reviews Dataset**
https://www.kaggle.com/zynicide/wine-reviews

---
# Notes from last meeting

As a group, we will go through how to get the data into DataBricks, how to set up a cluster, and how to read the data into your notebook

Example problems we will go through together as a group using Wine Reviews dataset - 1 problem together (10 mins)
Problem should show how to create a DataFrame
Should show some basic spark functions to give them clues to syntax
Explain the difference between using Spark functions and using spark SQL
Show how to view a DataFrame schema/how to import all the types

Wine Dataset problem;
Upload both tables
Start by calling .info() and .printSchema() on the dataframes
Select columns - country, designation, points, price, province, variety, 
Create reference table that is wine colour, and map the colours to wine names - this should be another dataframe that can be left-joined with the original dataset to add a ‘colour’ column to the main dataset
Drop rows with NA in the wine colour column
Filter out US from country - we don’t like their wine
Group by wine colour and get the average price, and max price for each colour
Turn points column into a new categorical column called rating - e.g. low-rated, mid-rated, high-rated 

--------------------------------------------------------------------------------------------------------------------------

Give me the maximum, minimum, and average fares for each class, excluding child passengers (Those under 18 years old)?
Give me a summary of the survival rate for each passenger gender survival rate as a %?



Bonus points - Pick and execute fill in the missing values for the cabin column? And explain why you have done it in this way?

