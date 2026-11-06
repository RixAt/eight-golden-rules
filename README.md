# Shneiderman's Eight Golden Rules

An interactive educational website exploring [Ben Shneiderman's](https://www.cs.umd.edu/~ben/index.html) [Eight Golden Rules of Interface Design](EIGHTRULES.md) through examples and quizzes.

## About the Project

This was originally developed as a group project for my Human-Computer Interaction class at Kent State University in Fall 2024.

## Project Status

I'm currently working on updating and restoring a live version of the website for posterity.
I might revisit some of the site design as well to improve my web development skills.

## Technologies

- HTML, CSS, JavaScript
- Node.js
- Express
- MySQL

## Original Setup Instructions
The following comes directly from the original project. I haven't verified that they are still applicable:

To run the code in browser, a few steps need to be done first:
1. Make sure Node.js and NPM are installed
2. Install MySQL and MySQL Workbench
3. In the MySQL Workbench, create a database named "mydb" and run the following SQL in it:
```sql
   CREATE TABLE users(
        id int NOT NULL AUTO_INCREMENT,
        username varchar(255),
        password varchar(255),
        PRIMARY KEY (id)
    );
    CREATE TABLE scores(
        id int NOT NULL,
        score int,
        PRIMARY KEY (id)
    );
```
5. Install the project dependencies using ```npm install```
6. Change the password variable in database.js line 11 to the password of root user that was set when setting up MySQL
7. Run the command ```node database.js```
8. Open a browser and navigate to ```http://localhost:3000``` or the port configured in the application
