# ds-grads-spark-training

## Getting Set Up on Databricks
1.	Go to https://databricks.com/try-databricks. You can connect to the _Stonehenge guest wifi network.
2.	Select ‘Get Started’ under the Community Edition.
3.	Sign-up using your personal email NOT your Lloyds email.
4.	Complete setup by verifying your email. NB the verification email may be in your spam.

## Demo
- As a group, we will go through how to navigate DataBricks, upload data, how to set up a cluster, and how to read the data into your notebook.
- For the Demo we'll being using Wine Review data (in WineDemo Folder), uploading the csv to Databricks and working through the notebook to familiarise ourselves with the syntax.

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
