# User API Spec

## Register User

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "angeline",
  "password": "rahasia",
  "name": "Angeline Lee"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "angeline",
    "name": "Angeline Lee"
  }
}
```

Response Body (Failed) :

```json
    "errors": "Username must not blank"
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username": "angeline",
  "password": "rahasia"
}
```

Response Body (Success) :

```json
{
  "data" : {
    "username" : "angeline",
    "name" : "Angeline Lee",
    "token" : "3cd1183a-116d-4c96-aee7-3caea32f43a7
"
  }
}
```

Response Body (Failed) :

```json
    "errors": "Username or password wrong"
```

## Get User

Endpoint : GET /api/users/current

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "username": "angeline",
  "name": "Angeline Lee"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "angeline",
    "name": "Angeline Lee"
  }
}
```

Response Body (Failed) :

```json
    "errors" : "Unauthorized"
```

## Update User

Endpoint : PATCH /api/users/current

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "password": "rahasia", // optional
  "name": "Angeline Lee" // optional
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "angeline",
    "name": "Angeline Lee"
  }
}
```

Response Body (Failed) :

```json
    "errors" : "Unauthorized"
```

## Logout

Endpoint : DELETE /api/users/current

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": "OK"
}
```

Response Body (Failed) :

```json
    "errors": "Unauthorized"
```
