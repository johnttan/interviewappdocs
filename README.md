# Interview Questions App
June 23, 2014
# Objectives
* Generate and manage questions in the interview process.
* Allow generation of questions by categories
* Minimal low-level interaction with the database and application. (No need to edit code or perform SQL queries to manage questions)
* Support several concurrent users and database of several thousand questions.
* Support IE 11+
* Run on IIS and with SQL Server 2012

# UI Outline + Key Features


* Sidebar
    * **Candidate Tab** (Hidden until candidate is selected or generated)
    * **Generate Tab** (For generating new portfolio of questions)
    * **Search Tab** (For searching through all questions and adding to current portfolio
    * **Update Tab** (For adding/deleting questions from the database)
    * **Update Keys** (For adding/removing categories/subcategories/roles)
    * **Previously Generated Tab** (Browse and manage previously generated portfolios)
    *
* Candidate Tab
    * **Print View button** (removes sidebar/buttons, reveals all questions)
    * List of questions by category.
    * Each question has
        * Button for revealing answer
        * Button for removing from current         portfolio

* Generate Tab
    * Required Field: Candidate Name
    * Fields: # of questions to generate per category
    *

