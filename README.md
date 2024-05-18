# nosql-challenge

# List of Content

1. NoSQL_setup_starter.ipynb

2. NoSQL_analysis_starter.ipynb

3. Folder of Resources containing a json file of establishments.json

Instructions

Part 1: Database and Jupyter Notebook Set Up

Use NoSQL_setup_starter.ipynb for this section of the challenge.

Import establishments.json file from Terminal. Name the database uk_food and the collection establishments. The command of "mongoimport --type json -d uk_food -c establishments --drop --jsonArray Resources/establishments.json" was also copied to a markdown cell in the Jupyter Notebook. 

-List the databases and Confirm that uk_food is listed.

-List the collection(s) in the database to ensure that establishments is there.

-Find and display one document in the establishments collection using find_one and display with pprint.
Assign the establishments collection to a variable to prepare the collection for use.

Part 2: Update the Database

Use NoSQL_setup_starter.ipynb for this section of the challenge.

Make changes to the establishments collection by adding the following information to the database:

{
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}
Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

Update the new restaurant with the BusinessTypeID.

Check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.

Use update_many to convert latitude and longitude to decimal numbers.
Use update_many to convert RatingValue to integer numbers.

Part 3: Exploratory Analysis

Eat Safe, Love has specific questions of finding the locations they wish to visit and avoid.

Use NoSQL_analysis_starter.ipynb for this section of the challenge.

RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.

The scores for Hygiene in reverse means the higher the value, the worse the establishment is in these areas.

Use the following questions to explore the database:

1. Use count_documents to display the number of documents contained in the result.

2. Display the first document in the results using pprint.

3. Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

4. Which establishments have a hygiene score equal to 20?

5. Which establishments in London have a RatingValue greater than or equal to 4?

6. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"? (Search within 0.01 degree on either side of the latitude and longitude.)

7. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

All those questions were answered in the file of NoSQL_setup_starter.ipynb