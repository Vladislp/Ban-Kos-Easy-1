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
    git clone https://github.com/Vladislp/Ban-Kos-Easy-1.git
    cd /Ban-Kos-Easy-1
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
## Start MongoDB

### MongoDB Setup

Using MongoDB Atlas:
1) Go to MongoDB Atlas.
2) Sign up or log in to your account.
3) Create a new cluster.
4) In the cluster, create a new database and a new user with access permissions.
5) Obtain the connection string from the "Connect" button in your cluster dashboard.

Using Local MongoDB:
1) Install MongoDB on your local machine from the official MongoDB website.
2) Start the MongoDB service.
3) Use the connection string mongodb://localhost:27017/your-database for your .env file.

### Set up environment variables:

1) Create a .env file in the root directory of the project.
2) Copy the contents of the .env.example file into your .env file.
3) Replace placeholder values with your actual MongoDB URI, secret key, and any other necessary environment variables.

### Example .env file:
```bash
MONGODB_URI=mongodb://<username>:<password>@<cluster-url>/<database>?retryWrites=true&w=majority
```
### Environment Variables Explanation

- `MONGODB_URI`: This is the connection string that your application uses to connect to the MongoDB database. It includes the username, password, cluster URL, and database name. Ensure that this string is kept secure and never hard-coded in your application files.

- `PORT`: This is the port number on which your backend server will run.

- `SECRET_KEY`: This is used for various purposes such as signing cookies or JWT tokens. Keep this value secret and secure.

###########################################################################################################

### If my .env is required, i can provide for you on request. Sharing somehow online is ... bad :)

###########################################################################################################

1) When cluster is ready, you should head to "Connect" section.
![1](https://github.com/user-attachments/assets/785b0f55-9c80-4559-a6e6-6357b71b4dfc)
2) Choose "Drivers"
![2](https://github.com/user-attachments/assets/98b60839-231a-434c-9d1c-26c2d437bfbd)
3) Under "Add your connection string into your application code" you will see you'r connection string to your MongoDB.
![3](https://github.com/user-attachments/assets/b769f46d-01f6-4b29-bbe3-0f5acaa52393)
4) Cloned project SHOULD NOT have .env file inside root folder. Create it and put inside your .env file.

        MONGODB_URI="connection string"
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

- **Get All Users:**
    ```http
    GET http://localhost:3000/users
    ```
- **Results:**
  
![image](https://github.com/user-attachments/assets/bbd4cc20-531d-4e15-896f-676d3afac651)

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

