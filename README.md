# Crowdfunding_ETL Project

## Introduction
ETL (Extract, Transform & Load) is a crucial skill in handling real-world data, often dispersed across multiple sources. This project focuses on the extraction, transformation, and loading of crowdfunding data to create a clean, accurate, and up-to-date dataset. The primary objective is to utilize ETL processes to manipulate, format, and enrich the data for meaningful insights.

### Sources of Data
Within the Resources Folder:
- `contacts.xlsx`
- `crowdfunding.xlsx`

### Database Type for Final Production Environment
The final production environment will utilize a Relational (SQL) database for efficient data storage and management.

- **Data Cleaning and Processing:** Jupyter Notebook
- **Packages Used:** pandas, numpy, datetime
- **Data Loading:** pgAdmin

An Entity Relationship Diagram (ERD) will be generated using a tool like [Quick Database Diagrams](https://www.quickdatabasediagrams.com/) to provide a visual representation of the database structure.

## ERD
![ERD](link-to-erd-image)

## Findings
1. The "theater" category has the highest success rate, while "Journalism" and "Games" have relatively low success rates.
2. The "plays" subcategory boasts the highest number of successful projects.
3. "Theater" has the highest sum of pledged amounts, followed by "film & video", "music", "publishing", and "technology".
4. The United States leads in total pledged amounts, followed by Canada and the United Kingdom.

## Conclusion
- Successful categories: "Theater," "Film & Video," and "Music."
- High success subcategories: "Plays," "Photography Books," "Web," "Food Trucks," and "Wearables."
- Leading countries in crowdfunding support: United States, Canada, and the United Kingdom.

## Project Outline

### 1. Create the Category and Subcategory DataFrames
   - Extract and transform data from `crowdfunding.xlsx` to create category and subcategory DataFrames.
   - Export as `category.csv` and `subcategory.csv`.

### 2. Create the Campaign DataFrame
   - Extract and transform data from `crowdfunding.xlsx` to create a campaign DataFrame.
   - Export as `campaign.csv`.

### 3. Create the Contacts DataFrame
   - Option 1: Use Python dictionary methods
     - Import `contacts.xlsx` into a DataFrame.
     - Convert each row to a dictionary and create a new DataFrame.
     - Split "name" into first and last names.
     - Export as `contacts.csv`.
   - Option 2: Use regular expressions
     - Import `contacts.xlsx` into a DataFrame.
     - Extract "contact_id," "name," and "email" using regular expressions.
     - Convert "contact_id" to the integer type.
     - Split "name" into first and last names.
     - Export as `contacts.csv`.

### 4. Create the Crowdfunding Database
   - Sketch ERD and create table schema in `crowdfunding_db_schema.sql`.
   - Create a new Postgres database named `crowdfunding_db`.
   - Create tables in the correct order with foreign keys.
   - Verify table creation and import CSV files.

## Instructions
Follow the outlined steps in each subsection of the project outline to successfully execute the Crowdfunding_ETL project.
