# Movie API

This is a simple RESTful API for managing movies. It allows you to perform CRUD operations (Create, Read, Update, Delete) on movie data. Below are the endpoints provided by this API:

## Endpoints

- `GET /movies`: Retrieve all movies.
- `GET /movies/{id}`: Retrieve a specific movie by its ID.
- `POST /movies`: Create a new movie.
- `PUT /movies/{id}`: Update an existing movie.
- `DELETE /movies/{id}`: Delete a movie.

## Data Structures

### Movie

Represents a movie entity.

#### Attributes

- `ID` (string): Unique identifier for the movie.
- `Isbn` (string): ISBN number of the movie.
- `Title` (string): Title of the movie.
- `Director` (object): Information about the director of the movie.

### Director

Represents information about the director of a movie.

#### Attributes

- `Firstname` (string): First name of the director.
- `Lastname` (string): Last name of the director.

## How to Use

1. **Retrieve all movies**: Send a GET request to `/movies` endpoint.

2. **Retrieve a specific movie**: Send a GET request to `/movies/{id}` endpoint, replacing `{id}` with the ID of the movie you want to retrieve.

3. **Create a new movie**: Send a POST request to `/movies` endpoint with the JSON payload containing movie details.

   Example JSON Payload:
   ```json
   {
       "isbn": "1234567890",
       "title": "New Movie",
       "director": {
           "firstname": "Jane",
           "lastname": "Doe"
       }
   }

4. **Update an existing movie**: Send a PUT request to /movies/{id} endpoint with the JSON payload containing updated movie details, replacing {id} with the ID of the movie you want to update.

   Example JSON Payload:
   ```json
   {
       "isbn": "1234567890",
       "title": "Updated Movie",
       "director": {
           "firstname": "Jane",
           "lastname": "Doe"
       }
   }

5. **Delete a movie**: Send a DELETE request to /movies/{id} endpoint, replacing {id} with the ID of the movie you want to delete.

## Starting the Server
To start the server, run the main function. The server will listen on port 8000.
- ``go run main.go``
