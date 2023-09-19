
# Note Taking WebApp

This was my CS50x final Project. I used Python, Flask, SQL, JavaScript to create this project.

## Video Demo:
Link: https://youtu.be/rnKmDO1zS9A?si=_FlaTBr1f36Bd6-x   <br>
<br>
<p align="center">
                Description
</p>



## base.html

It includes Bootstrap and Font Awesome libraries for styling and icons. It creates a navigation bar that changes its content based on whether a user is authenticated or not. It also handles and displays flash messages (error and success) and includes a JavaScript function for deleting a note with a POST request.
## home.html

This HTML template extends a base template, displaying a "Notes" heading along with a list of user notes, allowing users to delete individual notes, and providing a textarea and "Add Note" button for adding new notes to the list.
## login.html
This HTML template extends a "base.html" template with a "Login" title. It presents a login form with input fields for email and password, and a "Login" button for user authentication.
## sign_up.html

This HTML template extends a "base.html" template with a "Login" title but appears to be a "Sign Up" form. It includes fields for email, first name, and password, along with a password confirmation field, and a "Submit" button for user registration.
## __ init __.py
This Python code defines a Flask web application with SQLAlchemy for database management, Flask-Login for user authentication, and creates a SQLite database named "database.db." It registers two blueprints for different app views and models and sets up a user loader function for the login manager. Finally, it includes a function to create the database if it doesn't exist.
## auth.py
This Flask Blueprint, named "auth," contains routes for user authentication. It handles user login, logout, and registration, including input validation and flash messages for success or errors in the authentication process.
## models.py
This Python code defines two SQLAlchemy models: "Note" and "User." "Note" includes fields for note data, creation date, and a foreign key to associate notes with users. "User" includes fields for email, password, first name, and establishes a one-to-many relationship with notes using `db.relationship`. These models represent data structures for a web application with user authentication and note-taking functionality.
## views.py
The "views" Blueprint in Flask defines routes for an authenticated user's home page:

1. It allows users to add notes with input validation and stores them in the database.
2. It handles note deletion via POST requests, confirming user ownership.
3. Flash messages provide feedback for successful actions.
## main.py
This Python script creates a Flask web application using the "create_app" function from the "website" package, typically used to initialize the app. It then runs the app in debug mode if the script is executed directly.