<<<<<<< HEAD
# PRASHANT-ticket-management-system-api
=======

# Ticket Management System

This Ticket Management System, developed with Node.js and MongoDB, allows users to handle support tickets using CRUD operations (Create, Read, Update, and Delete). It demonstrates how to create a RESTful API using Express.js to handle a variety of ticket jobs. MongoDB serves as the database for storing and retrieving ticket data, showcasing efficient database interactions. The system allows users to generate new tickets, inspect current ones, edit details, and delete them as needed. This project demonstrates how to build scalable and adaptable backend systems with modern web development technologies.


## Features

                -Submit new support tickets for any issues or requests.
                -View all support tickets to track and manage ongoing or resolved cases.
                -Fetch a specific ticket by its unique identifier to see detailed information or status updates.
                -Modify a support ticket using its unique ID to update its details, such as the issue or priority.
                -Remove a support ticket using its unique ID once the issue is resolved or no longer relevant.
                -Ticket statuses include open (new or unresolved), in-progress (currently being worked on), and closed (resolved or completed). 
                -This system streamlines managing and tracking support tickets effectively.

## Project Setup

Prerequisites

    Node.js: Download and install Node.js
    MongoDB: Install MongoDB locally or use MongoDB Atlas for cloud-based hosting.

## Installation

1. Clone the repository:

                    git clone <repository-url>
                    cd <repository-folder>

2. Install project dependencies:

                    npm install

3. Environment Variables: Create a .env file in the root directory of your project with the following variables:

                  PORT=5000
                  MONGO_URI= mongodb+srv://dr1872002:Deepak3221@cluster0.jlnklez.mongodb.net/ticket-management-system

4. Run the project:

                 node index.js

5. Server will run on: 
                
                http://localhost:5000
## API Endpoints

1. Create a Ticket :-

    i) Endpoint:
    
                     POST /api/create-tickets

    ii) Description: Creates a new support ticket.

    iii) Request Body :
    
                   {
                      "title": "Issue with login",
                      "description": "User is unable to log in."
                   }

    iv) Response:

                  {
                       "_id": "64faacb8e1797e9a12345678",
                       "title": "Issue with login",
                       "description": "User is unable to log in.",
                       "status": "open",
                       "createdAt": "2024-09-20T12:00:00.000Z",
                       "updatedAt": "2024-09-20T12:00:00.000Z"
                  }


2. Get All Tickets :-

    i) Endpoint: 
       
                     GET /api/getAll-tickets

    ii) Description: Retrieves all tickets.

    iii) Response:

         {
             "totalCount": 9,
             "tickets": [
                        {
                            "_id": "64faacb8e1797e9a12345678",
                            "title": "Issue with login",
                            "description": "User is unable to log in.",
                            "status": "open",
                            "createdAt": "2024-09-20T12:00:00.000Z",
                            "updatedAt": "2024-09-20T12:00:00.000Z"
                        },
                          ...
                        ]
                   }




3. Get a Single Ticket :-

i) Endpoint: 
        
                    GET /api/single-tickets/:id

ii) Description: Retrieves a specific ticket by its unique ID.

iii)Path Parameter:

                  :id: The unique ID of the ticket.

iv)Response:

            {
                "_id": "64faacb8e1797e9a12345678",
                "title": "Issue with login",
                "description": "User is unable to log in.",
                "status": "open",
                "createdAt": "2024-09-20T12:00:00.000Z",
                "updatedAt": "2024-09-20T12:00:00.000Z"
            }


4. Update a Ticket :-

i) Endpoint: 
        
                   PUT /api/update-tickets/:id

ii) Description: Updates a ticket by its unique ID.

iii)Path Parameter:

                  :id: The unique ID of the ticket.

iv)Request Body (Any or all fields can be updated):

                  {
                     "title": "Updated title",
                     "description": "Updated description",
                     "status": "closed"
                  }




5. Delete a Ticket :-

i) Endpoint: 
        
                    DELETE /api/delete-tickets/:id

ii) Description: Deletes a ticket by its unique ID.

iii)Path Parameter:

                :id: The unique ID of the ticket.

iv)Response:

                  {
                    "message": "Ticket deleted successfully"
                  }





## Error Handling

400 Bad Request: 

    If required fields (title, description) are missing during ticket creation.

404 Not Found:
    If a ticket with the specified ID does not exist.

500 Internal Server Error: 
    For any server-side issues, the error message is returned in the response.


    
## Project Structure


    ├── config
    └── database.js   # Database config.

    ├── controllers
    └── ticketController.js   # Contains logic for ticket CRUD     operations

    ├── models
    │   └── ticketModel.js        # MongoDB schema for ticket

    ├── routes
    │   └── ticketRoutes.js       # API route definitions

    ├── .env                      # Environment variables (MongoDB     URI, port)

    ├── index.js                 # Main entry point of the application

    ├── package.json              # Project configuration and     dependencies
    
    └── README.md                 # Documentation

## Tools and Technologies

Node.js: 
    JavaScript runtime for building server-side applications.

Express.js: 
    Web framework for creating the API.

MongoDB:
 NoSQL database for storing ticket information.

Mongoose: 
    ODM library for MongoDB, used for schema modeling and interaction.

dotenv: 
    To manage environment variables.


## This README.md file now contains all the necessary details about your Ticket Management System project, including setup instructions, API endpoint documentation, and other important information.
>>>>>>> 07087ab (Initial commit)
