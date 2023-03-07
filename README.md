**We are building a website that allows users to search for movies and view details about them. Admin can do the same + add movies and delete them. 
GET /movies?title=: returns a list of movies that match the title.**
 ```
{
  "id": 1,
  "title": "Movie Title",
  "year": 2021,
  "genre": "Action",
  "description": "Movie description",
  "director": "Director name",
  "posterUrl": "https://example.com/poster.jpg"
}```


GET /movies?id=: returns the details of a single movie identified by its ID
{
  "id": 1,
  "title": "Movie Title",
  "year": 2021,
  "genre": "Action",
  "description": "Movie description",
  "director": "Director name",
  "posterUrl": "https://example.com/poster.jpg"
}

DELETE /movie/:id: removes a movie from movie ID
{
  "success": true
}

POST /movies/add: adds a new movie
Request:
{
  "title": "Movie Title",
  "year": 2021,
  "genre": "Action",
  "description": "Movie description",
  "director": "Director name",
  "posterUrl": "https://example.com/poster.jpg"
}

Response:
{
  "id": 3,
  "title": "Movie Title",
  "year": 2021,
  "genre": "Action",
  "description": "Movie Description",
  "director": "Director Name",
  "posterUrl": "https://example.com/poster.jpg"
}


POST /signup: creates a new user
Request:
{
  "username": "user",
  "password": "123"
}

Response:
{
  "token": "randomtoken."
}


POST /login: logs a user into their account and returns an authentication token
Request:
{
  "username": "user123",
  "password": "password123"
}

Response:
{
  "token": "randomtoken."
}


Entities:
User
Movie: attributes like title, release year, director, actors, and genre


Components:
Login.tsx
Logout.tsx
Movie.tsx
