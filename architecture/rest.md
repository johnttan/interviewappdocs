# REST

- - -
####Setup Endpoints
For setting up SQL database and default keys
- - -


####GET /setupsql

Sets up SQL table for questions

SQL:
*CREATE TABLE Questions ( question text, answers text, role text, subcategory text, category text, uid uniqueidentifier)*

####GET /setupkeys

Sets up SQL table for questions keys

SQL:
*CREATE TABLE Keys (json nvarchar(max))*
####GET /setuprecent

Sets up SQL table for recently generated candidates

SQL:
*CREATE TABLE Recent (hashedname nvarchar(max), json nvarchar(max))*

- - -
####Get Data Endpoints
For retrieving data from database
- - -

####GET /getquestions

Retrieves all questions

####GET /getkeys

Retrieves all keys

####GET /recent

Retrieves previous question portfolios

####GET /removerecent

This one is not for retrieving data.
This GET removes removes ALL recently generated candidates from database

- - -
####Add and Remove Data Endpoints
For updating entries in the database
- - -

####POST /addquestion

Adds question to table Questions

parameters:

**questionJSON** in request body. Refer to Model Structures chapter.

####POST /editquestion

Removes Question from table Questions

parameters:

{

            editType: edit
            question: questionJSON

}

####POST /insertkeys

Replaces data in table Keys

parameters:

####keysJSON in request body. Refer to Model Structures chapter.


####POST /insertrecent

Inserts new candidate into table Recent

parameters:

**userdataJSON** in request body. Refer to Model Structures chapter.

####POST /removerecent

Removes recent candidate from table Recent

parameters:

{

    hashedname: hashedname of candidate

}

####POST /updatrecent

Updates recent candidate data in table Recent

parameters:

**userdataJSON** in request body. Refer to Model Structures chapter.




