# To-Do List Web Application

A simple to-do list web application built with Node.js, Express, MongoDB, and EJS.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Future Improvements](#future-improvements)

## Project Overview

This is a basic web application that allows users to create and manage a list of to-do items. It provides a simple and intuitive user interface for adding tasks. The application is built on the MVC (Model-View-Controller) architecture, with a Node.js and Express backend, EJS for the views, and MongoDB for the database.

## Features

- **Create To-Do Items:** Add new tasks to your to-do list.
- **View To-Do Items:** See a list of all your to-do items. (Currently under development)
- **Edit To-Do Items:** Update the content of existing tasks. (Future feature)
- **Delete To-Do Items:** Remove tasks from your list. (Future feature)

## Technologies Used

- **Node.js:** A JavaScript runtime for building the backend.
- **Express.js:** A web application framework for Node.js.
- **MongoDB:** A NoSQL database for storing the to-do items.
- **Mongoose:** An Object Data Modeling (ODM) library for MongoDB.
- **EJS:** A simple templating language for generating HTML.
- **dotenv:** A module for loading environment variables from a `.env` file.
- **Nodemon:** A tool that automatically restarts the server during development.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or later)
- [npm](https://www.npmjs.com/) (usually comes with Node.js)
- [MongoDB](https://www.mongodb.com/try/download/community) (or a MongoDB Atlas account)

## Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/LoneWolf728/TodoApp.git
    cd todo-app
    ```

2.  **Install the dependencies:**

    ```bash
    npm install
    ```

3.  **Create a `.env` file:**

    Create a `.env` file in the root of the project and add your MongoDB connection string:

    ```
    DB_CONNECT=mongodb+srv://<username>:<password>@<cluster-name>.mongodb.net/<database-name>?retryWrites=true&w=majority
    ```

    Replace `<username>`, `<password>`, `<cluster-name>`, and `<database-name>` with your actual MongoDB credentials. You can find this connection string in the `mongodbinfo.txt` file.

## Usage

To start the application, run the following command:

```bash
npm start
```

This will start the server on `http://localhost:3000`. You can access the application by opening this URL in your web browser.

## Project Structure

```
.
├── .env
├── index.js
├── mongodbinfo.txt
├── package-lock.json
├── package.json
├── models/
│   └── TodoTask.js
├── node_modules/
├── public/
│   └── stylesheets/
│       └── style.css
└── views/
    └── todo.ejs
```

-   **`index.js`**: The main entry point of the application.
-   **`models/TodoTask.js`**: Defines the Mongoose schema and model for the to-do tasks.
-   **`views/todo.ejs`**: The EJS template for the user interface.
-   **`public/`**: Contains static assets like stylesheets.
-   **`.env`**: Stores environment variables, including the database connection string.
-   **`package.json`**: Lists the project's dependencies and scripts.

## API Endpoints

-   `GET /`: Renders the main to-do list page.
-   `POST /`: Creates a new to-do item.

## Future Improvements

-   Implement the ability to display all to-do items from the database.
-   Add functionality to edit existing to-do items.
-   Add functionality to delete to-do items.
-   Improve the user interface and add more styling.
-   Add user authentication to create personal to-do lists.
-   Add due dates and priority levels to the to-do items.
-   Write unit and integration tests for the application.
