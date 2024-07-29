# Node.js Express MongoDB API

This project is a simple Node.js application using Express.js to create a RESTful API and MongoDB for the database. It includes functionality to connect to a MongoDB database, define a schema and model using Mongoose, and create endpoints to interact with the data.

NB! This is my second repo, the thing is ... i made funny mistake in first repo. I can tell you more later :).

First repo commits

![image](https://github.com/user-attachments/assets/02d1347e-ef03-4477-bd79-e194a00bfc14)

First repo issues

![image](https://github.com/user-attachments/assets/e87feb3d-e95a-45f5-966c-ab6d9d2db5c9)



## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Project Structure](#project-structure)
- [Environment Variables](#environment-variables)
- [License](#license)

## Installation

1. **Clone the repository:**
    ```sh
    git clone [<repository-url>](https://github.com/Vladislp/Ban-Kos-Easy-1.git)
    cd <repository-directory>
    ```

2. **Install dependencies:**
    ```sh
    npm install
    ```

3. **Set up environment variables:**
    Create a `.env` file in the root of the project and add your MongoDB URI:
    ```plaintext
    MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
    ```

## Usage

1. **Start the server:**
    ```sh
    node app.js
    ```

2. **Server should be running on:**
    ```plaintext
    http://localhost:3000
    ```

3. **Use Postman or any API client to interact with the API.**

## Endpoints

- **Create a User:**
    ```http
    POST /users
    ```
    **Request Body:**
    ```json
    {
        "name": "John Doe",
        "email": "john@example.com",
        "age": 30,
        "hobbies": ["reading", "gaming"]
    }
    ```

- **Get All Users:**
    ```http
    GET /users
    ```

## Project Structure

/root

  ├── config
  
  │   └── db.js             # Database connection setup
  
  ├── models
  
  │   └── user-model.js     # Mongoose schema and model for User
  
  ├── routes
  
  │   └── users.js          # Express routes for User API
  
  ├── .env                  # Environment variables (make sure this is ignored by Git)
  
  ├── .gitignore            # Git ignore file
  
  ├── app.js                # Main application file
  
  ├── package.json          # Project metadata and dependencies
  
  └── README.md             # Project documentation



## Environment Variables

The following environment variables are used in this project:

- **MONGODB_URI**: The MongoDB connection string.

## License

This project is licensed under the MIT License.

