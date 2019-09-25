# ds-grads-spark-training

## Getting Set Up on Databricks
1.	Go to https://databricks.com/try-databricks. You can connect to the _Stonehenge guest wifi network.
2.	Select ‘Get Started’ under the Community Edition.
3.	Sign-up using your personal email NOT your Lloyds email.
4.	Complete setup by verifying your email. NB the verification email may be in your spam.

## Demo
....
## Exercise
Following the example queries on the Wine Review Dataset, you can now attempt the following.
1. Setting up the data
    - Download the data in the folder titanic-machine-learning-from-disaster.
    - Log into Databricks: https://community.cloud.databricks.com/login.html
    - Upload the datasets to DBFS data source under the folder: Filestore/tables.
2. Return to the home page and create a new workbook. 
3. Import the three csv files creating three spark dataframes.
4. Work through the following questions using some of the functions we saw in the wine review demo.
    - Explore the dataframes and datatypes.
    - Excluding the child passengers (Age < 18) find the the minimum, maximum, and average fares for each passenger class.
    - Produce a summary with the survival rates for each passenger gender, with survival rate as a %?
    - BONUS - Produce a summary of the passenger cabins. How will you handle missing values?

## Links required to do Spark hands-on session;

**DataBricks**
https://community.cloud.databricks.com/
https://docs.databricks.com/user-guide/notebooks/notebook-use.html

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
schema = t.StructType([t.StructField('Variety',t.StringType()), t.StructField('Colour',t.StringType())])
vals = [('Chardonnay','White'),('Pinot Noir','White'),('Cabernet Sauvignon','White'),('Riesling','White'),('Merlot','Red'),('Zinfandel','Red'),('Malbec','Red'),('Shiraz','Red'),('Sangiovese','Red')]
