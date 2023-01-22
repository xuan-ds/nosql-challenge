# Module_12_Challenge
## Background
### The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. This project is to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.
---
### Part 1: Database and Jupyter Notebook Set Up
#### Use `NoSQL_setup_starter.ipynb` for this section of the challenge.
1. Import the data provided in the `establishments.json` file from the Terminal. Name the database `uk_food` and the collection establishments. 
2. Import the libraries: PyMongo and Pretty Print (`pprint`).
3. Create an instance of the Mongo Client.
4. Confirm that the database has been created and the data has been loaded properly:
5. Assign the `establishments` collection to a variable to prepare the collection for use.

### Part 2: Update the Database
#### Use `NoSQL_setup_starter.ipynb` for this section of the challenge.
The magazine editors have some requested modifications for the database. Make the following changes to the `establishments` collection:
1. An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. Add the new restaurant into the database for analysis.
2. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the `BusinessTypeID` and `BusinessType` fields.
3. Update the new restaurant with the `BusinessTypeID`.
4. The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted
5. Some of the number values are stored as strings, when they should be stored as numbers. Use `update_many` to convert `latitude` and `longitude` to decimal numbers.

### Part 3: Exploratory Analysis
#### Use `NoSQL_analysis_starter.ipynb` for this section of the challenge.
Use the following questions to explore the database, and find the answers:
 - Use `count_documents` to display the number of documents contained in the result.
 - Display the first document in the results using `pprint`.
 - Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.
1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a `RatingValue` greater than or equal to 4?
3. What are the top 5 establishments with a `RatingValue` of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.