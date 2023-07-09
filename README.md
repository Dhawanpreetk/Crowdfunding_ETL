# Crowdfunding_ETL_Project

For the ETL mini project, ywe were to work with a partner to practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After transforming the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you’ll upload the CSV file data into a Postgres database.

**#Instructions**

The instructions for this mini project are divided into the following subsections:

Create the Category and Subcategory DataFrames
Create the Campaign DataFrame
Create the Contacts DataFrame
Create the Crowdfunding Database

**Create the Category and Subcategory DataFrames**

Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:

1."category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories

2."category" column that contains only the category titles

We Created the category DataFrame as below:(image)



**Extracted and transformed the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns**:****

 1."subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories

 2."subcategory" column that contains only the subcategory titles

The following image shows this subcategory DataFrame:

subcategory DataFrame (image):

**Create the Campaign DataFrame**
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

   "cf_id" column
   
   "contact_id" column
   
  "company_name" column
  
   "blurb" column, renamed to "description"
   
   "goal" column, converted to the float data type
   
  "pledged" column, converted to the float data type

"launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format

"deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format

"category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame

"subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

The following image shows this campaign DataFrame:

**Create the Contacts DataFrame**

Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:

Option 1: Use Python dictionary methods.

Option 2: Use regular expressions.

**Instructions for Option 1 which we choose:**

1.Import the contacts.xlsx file into a DataFrame.

2.Iterate through the DataFrame, converting each row to a dictionary.

3.Iterate through each dictionary, doing the following:

   1.Extract the dictionary values from the keys by using a Python list comprehension.
   2.Add the values for each row to a new list.
   3.Create a new DataFrame that contains the extracted data.
   4..Split each "name" column value into a first and last name, and place each in a new column.

4.Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.


**Create the Crowdfunding Database**

1.Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site..

2.Use the information from the ERD to create a table schema for each CSV file.
Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.

3.Create a new Postgres database, named crowdfunding_db.

4.Using the database schema, create the tables in the correct order to handle the foreign keys.

5.Verify the table creation by running a SELECT statement for each table.

6.Import each CSV file into its corresponding SQL table.

7.Verify that each table has the correct data by running a SELECT statement for each.
