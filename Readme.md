# Python Microservices

This repo contains python microservices for tests purpose

## Generator

* Run microservice
```bash
  cd generator
  docker build -t generator:v1 .
  docker run -d -p 8000:8000 --name generator generator:v1
```

* GET `/countries`

```bash
  curl localhost:8000/countries
```

```bash
[
  {
    "area": 513120, 
    "capital": "Bangkok", 
    "id": 1, 
    "name": "Thailand"
  }, 
  {
    "area": 7617930, 
    "capital": "Canberra", 
    "id": 2, 
    "name": "Australia"
  }, 
  {
    "area": 1010408, 
    "capital": "Cairo", 
    "id": 3, 
    "name": "Egypt"
  }
]
```

* POST `/countries`

```bash
HTTP/1.1 201 CREATED
Server: Werkzeug/2.1.1 Python/3.10.4
Date: Sun, 17 Apr 2022 20:28:35 GMT
Content-Type: application/json
Content-Length: 79

{
  "area": 357022, 
  "capital": "Berlin", 
  "id": 4, 
  "name": "Germany"
}

```