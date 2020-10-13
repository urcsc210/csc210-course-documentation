# Assignment 9: Databases

*Due: Tuesday, October 20, 2020 ...extra time!*

Your assignment is to add a database to your **Assignment 7 Recipe** application.

How exactly you complete the operation is up to you.  There are various techniques you can use, so long as your application fulfills the following requirements.

## Requirements

- You must use your **Recipe application** (Assignment 7) as a basis for this assignment
  - You can re-design/re-code the form however you want, but the goal is to leverage as much as you can off the old assignment
- The **functionality** of the application needs to do the following:
  - Store the entire ingredients list in an SQLite database - none of it can be hard-coded into the HTML
  - When the user fills out the form, the entered data must be <u>added</u> to the ingredients list in the database, and then displayed in an unordered list in the HTML
  - NOTE: we're only doing the "Create" and "Read" portions of the *four database functions* (C.R.U.D.); we'll implement Update and Delete later.
  - The optimal way to present the application is to have everything on one webpage.  However if you find that too difficult you can use two routes (webpages): one for data entry, and another to display the recipe (suboptimal but acceptable if need be)
- There needs to be a **requirements.txt** file in the application folder
  - All the dependencies - including the new ones from Chapter 5 - must be part of the new requirements file
  - IMPORTANT: The goal is to be able to re-create the virtual application environment (venv) to run the application on a different computer
- The database **model definition** must be written in Python, in one of your .py files
  - In the book, a model definition is shown in *hello.py* (p62), which you can follow, or use your own file structure - so long as the definition is in the app, somewhere
  - IMPORTANT: the goal is to be able to initialize the database for your application using Flask's **db.create_all()** function
- The database must use the *Alembic* **migration framework**
  - There must be a **migration** folder in your application file structure
  - IMPORTANT: the goal is to be able to re-create the database, including its data, using Flask's **flask db upgrade** command

## Video Tutorial

Besides the book (Chapter 5), there are many video tutorials that show you how to implement *Create* and *Read* database functions using Flask.  You're welcome to find one that helps you fulfill the requirements of this assignment.  

Here's is one that closely (but not perfectly) demonstrates the functionality required for Assignment 9:

- [Using Databases With Flask (YouTube)](https://youtu.be/hbDRTZarMUw)

*\* Yes - this is the same video that was embedded in the lecture video* 

## Turn-in Your Work

You are required to install your Assignment 8 app on the Web, and turn-in your ZIP'd application files via Blackboard

- Install Assignment 9 on your **UR Digital Scholar** website
- In our CSC 210 section in Blackboard, in **Assignment 9: Databases**, 
  - In the "Write Submission" box, paste the URL to your app on the Web
  - Upload a ZIP file containing your Assignment 9 files
