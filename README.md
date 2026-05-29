# ASP.NET Core Minimal API Basics

A beginner-friendly project for learning how to build a REST API using **ASP.NET Core Minimal APIs** and **C#**.

This repository is part of my journey to strengthen my .NET backend development skills by building a simple **To-Do API** with the minimum files, features, and dependencies required in ASP.NET Core.

## Project Goal

The goal of this project is to understand the fundamentals of building an API with ASP.NET Core, including:

* Creating API endpoints
* Handling HTTP requests and responses
* Working with route parameters
* Creating, reading, updating, and deleting data
* Understanding RESTful API operations
* Learning the Minimal API approach in .NET

## What is a Minimal API?

Minimal APIs are a lightweight way to create HTTP APIs in ASP.NET Core.

They are useful for:

* Small web APIs
* Microservices
* Beginner learning projects
* Applications that need a simple backend structure
* APIs that only need the essential dependencies and configuration

Instead of starting with controllers and several files, Minimal APIs allow endpoints to be defined directly in a simple application structure.

## API Overview

This project creates a To-Do API with the following endpoints:

| HTTP Method | Endpoint              | Description                       | Request Body       | Response Body                  |
| ----------- | --------------------- | --------------------------------- | ------------------ | ------------------------------ |
| `GET`       | `/todoitems`          | Get all to-do items               | None               | Array of to-do items           |
| `GET`       | `/todoitems/complete` | Get completed to-do items         | None               | Array of completed to-do items |
| `GET`       | `/todoitems/{id}`     | Get one to-do item by ID          | None               | To-do item                     |
| `POST`      | `/todoitems`          | Add a new to-do item              | To-do item         | Created to-do item             |
| `PUT`       | `/todoitems/{id}`     | Update an existing to-do item     | To-do item         | None                           |
| `PATCH`     | `/todoitems/{id}`     | Partially update an existing item | Partial to-do item | None                           |
| `DELETE`    | `/todoitems/{id}`     | Delete a to-do item               | None               | None                           |

## To-Do Item Example

A to-do item represents one task.

Example JSON object:

```json
{
  "id": 1,
  "name": "Learn ASP.NET Core Minimal APIs",
  "isComplete": false
}
```

## Technologies Used

* C#
* .NET
* ASP.NET Core Minimal API
* REST API principles
* Swagger / OpenAPI for API testing and documentation

## Getting Started

### Prerequisites

Before running this project, make sure you have installed:

* .NET SDK
* Visual Studio Code or Visual Studio
* Git

Check that .NET is installed:

```bash
dotnet --version
```

## Create the Project

Create a new ASP.NET Core web project:

```bash
dotnet new web -n TodoApi
```

Move into the project folder:

```bash
cd TodoApi
```

Run the application:

```bash
dotnet run
```

The terminal will display the local URL where the API is running.

Example:

```text
http://localhost:5000
https://localhost:7000
```

The exact port may be different on your computer.

## Example API Requests

### Get All To-Do Items

```http
GET /todoitems
```

Example response:

```json
[
  {
    "id": 1,
    "name": "Learn C# fundamentals",
    "isComplete": true
  },
  {
    "id": 2,
    "name": "Build my first Minimal API",
    "isComplete": false
  }
]
```

### Get Completed To-Do Items

```http
GET /todoitems/complete
```

### Get One To-Do Item

```http
GET /todoitems/1
```

### Create a To-Do Item

```http
POST /todoitems
```

Request body:

```json
{
  "name": "Practice ASP.NET Core",
  "isComplete": false
}
```

### Update a To-Do Item

```http
PUT /todoitems/1
```

Request body:

```json
{
  "id": 1,
  "name": "Practice ASP.NET Core Minimal APIs",
  "isComplete": true
}
```

### Partially Update a To-Do Item

```http
PATCH /todoitems/1
```

Example request body:

```json
{
  "isComplete": true
}
```

### Delete a To-Do Item

```http
DELETE /todoitems/1
```

## HTTP Methods Practiced

| Method   | Purpose                              |
| -------- | ------------------------------------ |
| `GET`    | Read data from the API               |
| `POST`   | Create new data                      |
| `PUT`    | Update an entire existing item       |
| `PATCH`  | Update only part of an existing item |
| `DELETE` | Remove an item                       |

## Learning Progress

* [ ] Create the ASP.NET Core Minimal API project
* [ ] Understand the default `Program.cs` file
* [ ] Add the To-Do model
* [ ] Add `GET /todoitems`
* [ ] Add `GET /todoitems/complete`
* [ ] Add `GET /todoitems/{id}`
* [ ] Add `POST /todoitems`
* [ ] Add `PUT /todoitems/{id}`
* [ ] Add `PATCH /todoitems/{id}`
* [ ] Add `DELETE /todoitems/{id}`
* [ ] Test the endpoints with Swagger
* [ ] Understand request bodies and response bodies
* [ ] Commit the completed project to GitHub

## What I Am Learning

Through this project, I am learning:

* The difference between C# and ASP.NET Core
* How a backend API receives requests
* How endpoints are mapped using Minimal APIs
* How JSON data is sent and received
* How CRUD operations work in a real API
* How HTTP methods represent different actions
* How to structure my first .NET backend project

## Future Improvements

After completing the basic tutorial, I plan to improve this API by adding:

* Input validation
* Better error handling
* A PostgreSQL database
* Entity Framework Core
* Authentication and authorization
* Docker support
* Unit tests
* GitHub Actions for automated builds

## Repository Purpose

This repository is a learning project focused on building a strong foundation in **ASP.NET Core backend development**.

It is part of my wider goal of becoming a professional software engineer capable of building secure web applications, APIs, dashboards, and business software systems.

## Author

**Nassim Namous**

Learning path: C# → ASP.NET Core → Angular → PostgreSQL → Docker → Full-Stack Business Applications
