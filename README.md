# Crowdfunding_ETL

Project presented by:
* Roberto Barrón
* Aldo Antonio Silva Espinoza
* Marcela Marilú Maldonado
* Marijose Cavazos

To perform the data cleaning, we utilized the following methods:

* Categories: Pandas, 
* Subcategories: Pandas,
* Campaigns: Pandas,
* Contacts: Pandas, and regular expressions (not used to export)

## Introduction

For this ETL mini project, we worked to practice building an ETL pipeline using Python, Pandas, and Python dictionary methods to extract and transform the data. 
After we transformed the data, we created four CSV files and use the CSV file data to create an ERD and a table schema. Finally, we uploaded the CSV file data into a Postgres database.
 
 ## Project logic
 The instructions for this mini project are divided into the following subsections:

### Create the Category and Subcategory DataFrames

We extracted and transformed the Excel data to create a category DF that has the following columns:
 *  category_id
 *  category
 
 We exported the category DF as category.csv and we saved it to the GitHub repository.
 We extracted and transformed the Excel data to create a subcategory DF that has the following columns:
 *  subcategory_id
 *  subcategory
 
 We exported the subcategory DF as subcategory.csv and we saved it to the GitHub repository.

### Create the Campaign DataFrame
We extracted and transformed the Excel data to create a campaign DF has the following columns:
* cf_id
* contact_id
* company_name
* description
* goal
* pledged 
* outcome
* backers_count
* country
* currency
* launch_date
* end_date
* category_id
* subcategory_id

We exported the campaign DF as campaign.csv and we saved it to the GitHub repository.

### Create the Contacts DataFrame

We iterated to create an output that matches the output given by pulling the dictionaries and splitting between lists for the coulmn names and the data within each row.

We cleaned the new dataframe by splitting first and last name and rearranging the orders.


### Create the Crowdfunding Database

From the CSV files we sketched and ERD of the tables using QuickDBD and with this info we created a table schema for each CSV file specifying the data types, primary keys and foreign keys.

We saved the database schema as a Postgres file named crowdfunding_db_schema.sql into the GitHub repository.

We verified the table creation by running a SELECT statement for each table, then we import each CSV file into its corresponding SQL table. 

Finally we verified that each table has the correct data by running a SELECT statement for each.

## Results

We created 3 folders to store the results:

* Resources: here we can find the csv files that we used to create the DataFrames.
*
* DataFrames: here we can find the outputs of the jupyter notebooks.
* 
* SQL Querys : here we can find the ERD, the table schemas and sql database.


* Note: Please find the SQL-related files under the SQL folder.

## Analysis conclusion:
   It is very common to have unorganized, not ready to use databases that may seem like they are useless because of the structure they were given. Using pandas or regular expressions we can give those datasets a good structure to give them back to the client for them to use with ease. Even though we did not analyze the information per say, only by cleansing and re structuring the data has an added value to the client. Further analysis may be done by having the shareholder's input on what they're looking for specifically. We had some difficulties when trying to create the database but solved the issue using pgAdmin. 

