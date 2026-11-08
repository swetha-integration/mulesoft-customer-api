# MuleSoft Customer Management API

## Project Overview

The MuleSoft Customer Management API is a RESTful API developed using MuleSoft Anypoint Studio. It provides endpoints to create, retrieve, update, and delete customer records.

The project demonstrates REST API development, HTTP Listener configuration, DataWeave transformations, Object Store operations, and error handling.

## Features

- Create a new customer
- Retrieve all customers
- Retrieve a customer by ID
- Update an existing customer
- Delete a customer
- Store and retrieve customer records using MuleSoft Object Store
- Handle missing customer records with appropriate HTTP status codes and JSON error responses

## Technology Stack

- MuleSoft Anypoint Studio 7.21
- Mule Runtime 4.9.2
- Anypoint Object Store Connector 1.3.4
- DataWeave 2.0
- REST APIs
- HTTP Listener
- Postman
- Git and GitHub

## API Endpoints

| HTTP Method | Endpoint              | Description               |
| ----------- | --------------------- | ------------------------- |
| POST        | `/api/customers`      | Create a customer         |
| GET         | `/api/customers`      | Retrieve all customers    |
| GET         | `/api/customers/{id}` | Retrieve a customer by ID |
| PUT         | `/api/customers/{id}` | Update a customer         |
| DELETE      | `/api/customers/{id}` | Delete a customer         |

## Implementation Details

### Object Store

MuleSoft Object Store is used to persist customer records. Each customer is stored using a unique customer ID as the key, allowing records to be retrieved, updated, and deleted individually.

### DataWeave

DataWeave 2.0 is used to transform payloads and produce JSON responses.

### Error Handling

The API handles scenarios where a requested customer ID does not exist and returns an appropriate HTTP 404 response with a JSON error message.

## Running the Project

1. Clone this repository.
2. Open the project in Anypoint Studio.
3. Configure the required Mule runtime.
4. Run the Mule application.
5. The API will be available locally at:

   `http://localhost:8081`

## Testing

The API endpoints can be tested using Postman.

Example requests:

- `GET http://localhost:8081/api/customers`
- `GET http://localhost:8081/api/customers/4`
- `POST http://localhost:8081/api/customers`
- `PUT http://localhost:8081/api/customers/4`
- `DELETE http://localhost:8081/api/customers/4`

Sample POST Request Body

{
  "id": "5",
  "name": "Swetha",
  "email": "swetha@example.com"
}

Sample PUT Request Body

{
  "id": "4",
  "name": "Updated Customer",
  "email": "updated@example.com"
}

Set the request header:

Content-Type: application/json

## Author

Swetha

## Repository

[GitHub - MuleSoft Customer Management API](https://github.com/swetha-integration/mulesoft-customer-api)
