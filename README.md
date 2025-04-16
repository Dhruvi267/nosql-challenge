# MongoDB Data Analysis for Restaurant Hygiene and Ratings

## Overview

This project focuses on analyzing food hygiene ratings of establishments across the United Kingdom. The goal is to help **Eat Safe, Love** magazine focus on the most relevant establishments for future articles, by evaluating hygiene scores and their correlation with factors like location and rating values.

## Objectives

- **Database Setup**: Import food establishment data into MongoDB.
- **Data Modifications**: Add new data entries, remove irrelevant entries, and convert fields (e.g., latitude, longitude) to the correct data type.
- **Exploratory Analysis**: Perform various analyses to identify notable establishments for future magazine articles.

## Project Steps

### Part 1: Database and Jupyter Notebook Setup

1. **Data Import**: Import the `establishments.json` file into MongoDB.
   ```bash
   mongoimport --drop --db uk_food --collection establishments --file "/path/to/establishments.json" --jsonArray
   ```

2. **MongoDB Connection**: Use **PyMongo** in Jupyter Notebook to connect to MongoDB.

### Part 2: Data Modifications

1. **Add a New Restaurant**: Insert the new restaurant "Penang Flavours" into the database.
2. **Data Cleaning**: Remove establishments from Dover and convert latitude/longitude fields to decimal.

### Part 3: Exploratory Data Analysis

1. **Hygiene Score Analysis**: Identify establishments with a hygiene score of 20.
2. **London Establishments**: Find establishments in London with a RatingValue of 4 or greater.
3. **Top 5 Establishments**: Identify the top 5 establishments with a RatingValue of 5, sorted by hygiene score.
4. **Aggregation of Hygiene Scores**: Count the number of establishments in each local authority area with a hygiene score of 0.

## Results and Analysis

After executing the queries and performing the analysis, we will produce key insights that the editorial team of Eat Safe, Love can use to decide which establishments to focus on for their articles. Key results include:

Number of establishments in London with a RatingValue of 4 or higher.

The top 5 establishments with the highest hygiene ratings and proximity to "Penang Flavours."

A list of local authority areas with a significant number of establishments having a hygiene score of 0.

## Conclusion

This project provides a comprehensive analysis using MongoDB and Python tools, enabling **Eat Safe, Love** to efficiently explore and analyze food hygiene data.The use of MongoDB for data management and PyMongo for querying the database allows for efficient exploration and manipulation of the dataset.
