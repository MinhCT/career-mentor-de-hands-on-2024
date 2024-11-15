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
- Programming Language (Nice to have)
- Database
- SQL

Nice to have:
- A non-work email address to register cloud account
- An existed Threads account
- Working on any Cloud platform before

## Day 0: Video guide creating accounts:
- Create free account on Snowflake Cloud
- Create ready-to-use (2) developer accounts in Threads

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
    - Snowflake Datawarehouse
- Align everyone to have the same prerequisites
- Explain the Extraction process
  - Why doing data extraction?
  - List out some examples of data extraction
- Hands-on day 1:
  - Use provided code snippet to the Notebook
  - Integrate the access token into the code snippet
  - Run and observe the result
  - Sneakpeak the problems with this Extraction

## Day 2: Load
- Explain why we need to manual trigger notebook to crawl data:
  - There is no place to store the data after crawling
  - And the data is in hard-to-read format (JSON)
- Basic walkthrough of data loading:
  - Introduce data storage, database
  - Introduce Snowflake - a datawarehouse solution
  - Explain that we will have to modify the Notebook to perform loading to Snowflake
- Hands-on day 2:
  - Use code snippet to create schema + table
  - Use code snippet to update Notebook to store data to Snowflake
  - Examine loaded data in Snowflake by executing SQL statement
  - Sneakpeak the problems with this Loading

## Day 3: Transform
- Walkthrough the use case of grouping data in Snowflake to use in something useful
- Hands-on day 3:
  - Implement a SQL to aggregate through the Threads data
  - Identify the problem of running this SQL everytime
  - Design a table to store transformed data
  - Create physical table in Snowflake
  - Walkthrough the usage of CTAS statement that combine SQL transform logic with creating table
- Wrap-up the 3-days experience
