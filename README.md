# family_travel_tracker

This is a simple web application built with Express.js and PostgreSQL that tracks the countries a user has visited. Users can add visited countries and switch between different users.

## Features

- Add visited countries based on partial country name.
- Display a list of all countries a user has visited.
- Switch between users or create a new user with a preferred color.

## Technologies Used

- **Node.js** with **Express.js**
- **PostgreSQL** database
- **EJS** templating engine
- **Body-parser** middleware

## Prerequisites

  Make sure you have the following installed:

- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)

## Install the dependencies:
   npm install

## Set up PostgreSQL:

    Create a PostgreSQL database.
    Run the SQL schema to create the necessary tables.

    CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    color VARCHAR(20)
    );
    
    CREATE TABLE countries (
        id SERIAL PRIMARY KEY,
        country_code VARCHAR(3),
        country_name VARCHAR(100)
    );
    
    CREATE TABLE visited_countries (
        id SERIAL PRIMARY KEY,
        country_code VARCHAR(3),
        user_id INT REFERENCES users(id)
    );

  ## Run the application:
      node inde.js

  ![image](https://github.com/user-attachments/assets/520dd01d-73d2-44a8-b431-dd6410b52c49)
  ![image](https://github.com/user-attachments/assets/7d82616d-e44c-4a9b-a5af-45615ae55ad7)

