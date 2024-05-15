# Coursework_OOP
Repository for keeping all the information aboute course project - web-application, that contains information about films.

# Functional requirements:
-	As a user, I want to be able to look at films on main page
-	As a user, I want to look at specific film information page
-	As a user, I want to be able to search film by a name 
-	As a user, I want to be able to search film by a rate
-	As a user, I want to be able to search film by a release date
-	As a user, I want to be able to rate films
-	As a user, I want to be able to create and delete lists for films
-	As a user, I want to be able to open list and see its containment
-	As a user, I want to be able to find lists by name
-	As a user, I want to be able to add and remove films from lists
-	As an admin, I want to be able to add films
-	As an admin, I want to be able to change film information


# Database

[Database](database.PNG)

# REST API endpoints

Get specific film information
Endpoint: GET /films/{filmId}
Path Parameter: filmId

Search films by name
Endpoint: GET /films/search
Query Parameter: name 

Search films by rate
Endpoint: GET /films/search
Query Parameter: rate

Search films by release date
Endpoint: GET /films/search
Query Parameter: release_year

Rate a film
Endpoint: POST /films/{filmId}/rate
Path Parameter: filmId (ID of the film)
Request Body:
{
  "rating": number
}

Create a list
Endpoint: POST /lists
Request Body:
{
  "name": string
}

Delete a list
Endpoint: DELETE /lists/{listId}
Path Parameter: listId 

Get list contents
Endpoint: GET /lists/{listId}
Path Parameter: listId 

Find lists by name
Endpoint: GET /lists/search
Query Parameter: list_name

Add a film to a list
Endpoint: POST /lists/{listId}/films
Path Parameter: listId
Request Body:
{
  "filmId": number
}

Remove a film from a list
Endpoint: DELETE / lists/{listId}/films
Path Parameter: listId 
Request Body:
{
  "filmId": number
}

Add a film
Endpoint: POST /admin/films
Request Body:
{
 "name": string,
 "release_year": number (date),
 "lenght": number (timestamp),
 "description": string
}

Update film information
Endpoint: PUT /admin/films/{filmId}
Path Parameter: filmId
Request Body:
{
  "name": string,
  "release_year": number (date),
  "lenght": number (timestamp),
  "description": string
}
