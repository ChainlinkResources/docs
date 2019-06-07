# Users

## List Users

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users
HTTP/2 200
```


> Response JSON:

```json
[
  {
        "id": "7fc90f5a-45e3-42ed-84b9-c13aed6481f1",
        "created_at": "2018-10-09T02:29:30.580961Z",
        "name": "EntArchitect",
        "email": "big-arch@example.com",
        "password": "$2a$10$TzD5muUNH0BFrfwwzsuthOlipQ45e5q3ba8l8wIB9ESPD4d5z/e5G"
    },
    {
        "id": "876e4fc6-b379-432c-8f76-7e42a955d527",
        "created_at": "2018-10-09T02:21:14.531578Z",
        "name": "SavvyExec",
        "email": "vip@example.com",
        "password": "$2a$10$5ebxXX.iWe7OMOHr5CGeye6.G/uj3sb4gRzXxyCEYI2B6KCFYRrz."
    }
]
```

This endpoint enumerates previously created Users for the authorized Application.

### HTTP Request

`GET /api/v1/users`


## Post Users


```shell
curl -i -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users \
    -d '{"name": "SavvyExec", "email": "vip@example.com", password": "Str0ngPa55w0rd"}'
HTTP/2 201
```


> Response JSON:

```json
[
  {
    "id": "876e4fc6-b379-432c-8f76-7e42a955d527",
    "created_at": "2018-10-09T02:21:14.531577683Z",
    "name": "SavvyExec",
    "email": "vip@example.com"
}
]
```

This endpoint creates a new platform User or a User on behalf of an authorized Application.

### HTTP Request

`POST /api/v1/users`


## Update Users


```shell
curl -i -XPUT \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users/876e4fc6-b379-432c-8f76-7e42a955d527 \
    -d '{"name": "Professional Executive"}'
HTTP/2 204
```


This endpoint updates an existing User record.

### HTTP Request

`PUT /api/vi/users/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | id of the Application


## Delete Users


```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users/876e4fc6-b379-432c-8f76-7e42a955d527
HTTP/2 501
```


> Response JSON:

```json
[
  {
    "message": "not implemented"
}
]
```

This endpoint removes a User record.

<i> (Not yet implemented)</i>

### HTTP Request

`DELETE /api/vi/users/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | id of the Application
