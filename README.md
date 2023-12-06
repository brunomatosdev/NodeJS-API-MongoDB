Node.js API with Express and MongoDB

This repository contains a simple Node.js API built using Express and MongoDB. The API provides endpoints for managing a collection of resources, and it's intended to serve as a starting point for developing more complex applications.
Prerequisites

Before you begin, ensure you have the following installed on your machine:

    Node.js
    npm (Node.js package manager)
    MongoDB (Make sure MongoDB is running on your local machine or update the connection details in config.js)

Getting Started

    Clone the repository:

    bash

git clone https://github.com/brunomatosdev/NodeJS-API-MongoDB

Navigate to the project directory:

bash

cd node-express-mongodb-api

Install dependencies:

bash

npm install

Start the application:

bash

    npm start

    The API will be accessible at http://localhost:3000.

API Endpoints
Get All Resources

    URL: /resources
    Method: GET
    Response:

    json

    [
      {
        "_id": "60f4f35b8b105e001731e32f",
        "name": "Resource 1",
        "description": "This is the first resource."
      },
      {
        "_id": "60f4f35b8b105e001731e330",
        "name": "Resource 2",
        "description": "This is the second resource."
      }
    ]

Get a Specific Resource

    URL: /resources/:id
    Method: GET
    Response:

    json

    {
      "_id": "60f4f35b8b105e001731e32f",
      "name": "Resource 1",
      "description": "This is the first resource."
    }

Create a New Resource

    URL: /resources
    Method: POST
    Request:

    json

{
"name": "New Resource",
"description": "This is a new resource."
}

Response:

json

    {
      "_id": "60f4f35b8b105e001731e331",
      "name": "New Resource",
      "description": "This is a new resource."
    }

Update a Resource

    URL: /resources/:id
    Method: PUT
    Request:

    json

{
"name": "Updated Resource",
"description": "This resource has been updated."
}

Response:

json

    {
      "_id": "60f4f35b8b105e001731e331",
      "name": "Updated Resource",
      "description": "This resource has been updated."
    }

Delete a Resource

    URL: /resources/:id
    Method: DELETE
    Response:

    json

    {
      "_id": "60f4f35b8b105e001731e331",
      "name": "Updated Resource",
      "description": "This resource has been updated."
    }

Configuration

The MongoDB connection details can be configured in the config.js file. Update the dbUrl variable with the appropriate MongoDB connection string.

javascript

module.exports = {
dbUrl: 'mongodb://localhost:27017/yourdatabase',
};

Contributing

Feel free to contribute to this project by submitting issues or pull requests. Your feedback and contributions are highly appreciated!
License

This project is licensed under the MIT License - see the LICENSE file for details.
