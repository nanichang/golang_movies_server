# Golang Movie Server

### - Getting started
- Clone the project at `git@github.com:nanichang/golang_movies_server.git`
- Build the project by running `go build`
- Run the project with `go run main.go`
- Access the project via browser at `http://localhost:8000/movies`

#### - Routes

##### 1: Get All Movies
**URL:** `http://localhost:8000/movies`
**METHOD:** `GET`
**RESPONSE:**

```
[
    {
        "id": "1",
        "isbn": "438227",
        "title": "Black Panther",
        "director": {
            "firstname": "Nani",
            "lastname": "Paul"
        }
    },
    {
        "id": "2",
        "isbn": "438627",
        "title": "Black Adam",
        "director": {
            "firstname": "James",
            "lastname": "Bond"
        }
    }
]
```

___

##### 2: Get a Movie by ID
**URL:** `http://localhost:8000/movies/1`
**METHOD:** `GET`
**RESPONSE:**
```
{
    "id": "1",
    "isbn": "438227",
    "title": "Black Panther",
    "director": {
        "firstname": "Nani",
        "lastname": "Paul"
    }
}
```

##### 3: Create a Movie
**URL** `http://localhost:8000/movies`
**METHOD:** `POST`
**REQUEST BODY:**
```
{
    "isbn": "438228",
    "title": "Black Widow",
    "director": {
        "firstname": "Viva",
        "lastname": "Paul"
    }
}
```
**REPONSE:**
```
{
    "id": "98498081",
    "isbn": "438228",
    "title": "Black Widow",
    "director": {
        "firstname": "Viva",
        "lastname": "Paul"
    }
}
```

##### 4: Update a Movie
**URL:** `http:localhost:8000/movies/98498081`
**METHOD:** `PUT`
**REQUEST BODY:**
```
{
    "isbn": "438228",
    "title": "Black Widow",
    "director": {
        "firstname": "Viva",
        "lastname": "Marvel"
    }
}
```

**RESPONSE:** 
```
{
    "id": "98498081",
    "isbn": "438228",
    "title": "Black Widow",
    "director": {
        "firstname": "Viva",
        "lastname": "Marvel"
    }
}
```
##### 5: Deleting a Movie
**URL:** `http:localhost:8000/movies/98498081`
**METHOD:** `DELETE`
**RESPONSE:**
```
[
    {
        "id": "1",
        "isbn": "438227",
        "title": "Black Panther",
        "director": {
            "firstname": "Nani",
            "lastname": "Paul"
        }
    },
    {
        "id": "2",
        "isbn": "438627",
        "title": "Black Adam",
        "director": {
            "firstname": "James",
            "lastname": "Bond"
        }
    }
]
```