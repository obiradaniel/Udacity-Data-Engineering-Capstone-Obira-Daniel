# Udacity Data Engineering Capstone Project: Analysis and Pipelines for Immigration data to US

### ***Udacity Data Engineering Course 5: Data Engineering Capstone Project***
### ***Final Course Project Assignment***

***
In a NutShell Parquet is a Hero.

Processing All US Visitors in March 2016, about 3,157,072 People from Raw SAS data to some few insights.

The project follows the follow steps:

Step 1: Scope the Project and Gather Data

Step 2: Explore and Assess the Data

Step 3: Define the Data Model

Step 4: Run ETL to Model the Data

Step 5: Complete Project Write Up

This project transforms SAS data to Parquet,  Pushes it to S3, cleans, renames columns and
then exports to final parquet for futher upstream analysis and creates functions to do that.

Some simple Analysis is done for the month of March 2016, some 3,157,072 Passengers, 
the insights are then joined to spatial data to make simple maps.

To analyse even just 2-3 months you will need EMR.
Total data for the whole year is 40,790,529 Records.

The whole project is mainly on the Udacity Workspace and based on PySpark, Boto3, Matplotlib, 
Pandas and GeoPandas for the mapping.
***
## Contents: 
1. Data to be used: 
    1. Mainly I94 Immigration data, it's metadata and some spatial data. 

***
Folders:
 1. sas_data_raw/2016/03 - Raw Parquet from SAS Export
 2. sas_data_final/2016/03 - Processed Parquet ready for Upstream Analysis
 3. Mapping - Files for Integration into Parquet
 4. Pictures - Key Project Pictures
 5. Analysis_Output - CSv output from analytical PySpark Queries for GIS Mapping
 6. GIS - Shapefiles for Mapping

***
Changes after FeedBack from Reviewer:
 1. Pipelines Schedules should be monthly because the i94 summary data is posted mothly.
 Depending on the day that data is normally posted the DAG can run a day after with,
  3-5 retries with 12 hours to a day retry interval.
 2. Added details on how to handle the data increase by 100X ,
 and the technical implementation overview of such an increase in data.
 3. Removed the Extra Cells after the Data Dictionary

***
### To run
### 1. update 'dwh.cfg' with the right AWS credentials 
### 2. Work all the PySpark on Udacity WorkSpace, Export the outputs for Mapping
### 3. Download the NoteBook and outputs from the Udacity WorkSpace and 
### then do the GIS using GeoPandas on your local machine.
### Options
### You can use EMR if you have pushed the parquet to S3.

## S3 Bucket with monthly Raw Parquet Data 2016
![S3 Raw Bucket](https://raw.githubusercontent.com/obiradaniel/Udacity-Data-Engineering-Capstone-Obira-Daniel/master/Pictures/Raw_S3_bucket.png)

## Numerical Variable Distribution
![Numbers Dist](https://raw.githubusercontent.com/obiradaniel/Udacity-Data-Engineering-Capstone-Obira-Daniel/master/Pictures/Numerical_dist.png)

## Data Schema
![Schema](https://raw.githubusercontent.com/obiradaniel/Udacity-Data-Engineering-Capstone-Obira-Daniel/master/Pictures/Data_Schema.png)

## Key Categorical Value Distribution
![Categorical Values](https://raw.githubusercontent.com/obiradaniel/Udacity-Data-Engineering-Capstone-Obira-Daniel/master/Pictures/Categorical_dist.png)

## World Map showing US Visitors March 2016
![World Map](https://raw.githubusercontent.com/obiradaniel/Udacity-Data-Engineering-Capstone-Obira-Daniel/master/Pictures/US_visitors.png)

## US State Map by Visitors 2016
![US State Map](https://raw.githubusercontent.com/obiradaniel/Udacity-Data-Engineering-Capstone-Obira-Daniel/master/Pictures/Visitors_US_States_March_2016.png)

## Airport Map by Visitors March 2016
![Airport Map](https://raw.githubusercontent.com/obiradaniel/Udacity-Data-Engineering-Capstone-Obira-Daniel/master/Pictures/Airports_US.png)


### ***Obira Daniel, December 2022***
