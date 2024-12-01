# User Registration Endpoint

## Endpoint

`POST /user/register`

## HTTP Method

`POST`

## Description

This endpoint allows a new user to register by providing their first name, last name, email, and password.

## Request Body

The request body should be a JSON object with the following structure:

```json
{
  "fullname": {
    "firstname": "First name",
    "lastname": "Last name"
  },
  "email": "user@example.com",
  "password": "password"
}
```

## Exampple Response

- `user` (object):

  - `fullname` (object).
    - `firstname` (string,required): User's First name (Min 3 chars).
    - `lastname` (string,optional): User's Second name (Min 3 chars).
  - `email` (string,required): User's email address (must be a valid email).
  - `password` (string,required): User's password (min 6 chars).

- `token` (string): JWT Token

{
"errors": [
{
"msg": "Error message",
"param": "field name",
"location": "body"
}
]
}
