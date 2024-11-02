# Data Engineer Hands On Program Outline

## Overview
This reading intends to describe the general outline of what will be shared during the 3-days event of the Data Engineer Hands On Program hosted by Career Mentor.

### What's will be covered
Over the course of the 3-days sharing session, we expect to share the following topics:
- Some getting started theories about:
  - What is Data Engineering?
  - Data Pipeline and ELT (previously ETL)
  - Simple techniques to design data pipeline
- Skills honing
  - Small challenges during each sharing session:
    - Quizzes
    - Fill code in the blank
    - Simple question
  - Hands On Project: *Simple data pipeline for Meta's Threads*
- Format
  - The hands-on project will be dominant, and from doing the project, session participants can understand more about each letter in the whole ELT process
  - Each day will cover exactly one later in the "ELT" process
  - Due to limited time, all of the code and hands-on experiences will be perform on Cloud, with the following tools have been considered:
    - Anaconda Cloud Notebook
    - Snowflake Datawarehouse
    - dbt Cloud
  - The code for the whole course will be prepared and stored in the same repository as this README.md file

## Prerequisites
The registered participants are recommended to have basic understands of the following topics:
- Python
- Database
- SQL

Nice to have:
- A non-work email address to register cloud account
- An existed Threads account
- Working on any Cloud platform before

## Day 1: Extraction
- Introduction about the experience
- Basic theories walkthrough
  - What is Data Engineering?
  - Data Pipeline and ELT (or ETL)
- Introduce the Hands On project:
  - What is the project about?
  - What is the final result look like?
  - What are steps need taken to have the similar result?
  - Explain the hands-on approach and useful tools:
    - Anaconda Cloud Notebook
    - Snowflake Datawarehouse
    - dbt Cloud
- Align everyone to have the same prerequisites
- Explain the Extraction process
  - Why doing data extraction?
  - List out some examples of data extraction
- Hands-on day 1:
  - Create a free account to setup Anaconda Notebook
  - Create/Update developer account in Threads
  - Create an access token for client app to use
  - Use provided code snippet to the Notebook
  - Integrate the access token into the code snippet
  - Run and observe the result
  - Sneakpeak the problems with this Extraction

## Day 2: Load
- Introduce Batch Processing vs Stream Processing
- Explain the drawback of manual trigger notebook to crawl data
  - Have to do it manually
  - There is no place to store the data after crawling
- Basic walkthrough of data loading:
  - Introduce data storage, database
  - Introduce Snowflake - a datawarehouse solution
  - Explain that we will have to modify the Notebook to perform loading to Snowflake
- Hands-on day 2:
  - Explain what we are going to do is a Batch Processing
  - Create free account on Snowflake Cloud
  - Design table to store crawled Threads data
  - Create schema and phyiscal table with SQL
  - Create user to connect to Snowflake
  - Use code snippet to update Notebook to store data to Snowflake
  - Schedule a job to run Notebook periodically
  - Examine loaded data in Snowflake by executing SQL statement
  - Sneakpeak the problems with this Loading

## Day 3: Transform
- Walkthrough the use case of grouping loaded data in Snowflake to use in something useful
- Hands-on day 3:
  - Implement a SQL to aggregate through the Threads data
  - Identify the problem of running this SQL everytime
  - Design a table to store transformed data
  - Create physical table in Snowflake
  - Walkthrough the usage of CTAS statement that combine SQL transform logic with creating table
  - Explain the big drawbacks of just using SQL to transform data:
    - SQL is stored in Snowflake, no version control and hard to maintain
    - Hard to scale
    - Hard to apply frameworks or best practices from Software Engineering
  - Introduction to dbt
  - Create new dbt Cloud account
  - Setup new dbt project
  - Setup credentials to connect to Snowflake
  - Migrate SQL to dbt model using code snippet
  - Run to create the model once
  - Schedule a job to periodically run dbt model to update transformed data
  - Use code snippet Notebook to connect to transformed table and plot a simple dashboard
- Wrap-up the 3-days experience